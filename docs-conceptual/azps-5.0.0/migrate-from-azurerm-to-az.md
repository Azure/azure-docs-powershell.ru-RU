---
title: Перенос скриптов Azure PowerShell с AzureRM на Az
description: Сведения о действиях и инструментах для переноса скриптов с модуля AzureRM на новый модуль Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753878"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="462f0-103">Перенос Azure PowerShell с AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="462f0-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="462f0-104">Все версии модуля AzureRM PowerShell устарели, но все еще поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="462f0-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="462f0-105">[Модуль Az PowerShell](install-az-ps.md) теперь является рекомендуемым модулем PowerShell для взаимодействия с Azure.</span><span class="sxs-lookup"><span data-stu-id="462f0-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="462f0-106">Скрипты, написанные для командлетов AzureRM, не смогут автоматически работать с новым модулем.</span><span class="sxs-lookup"><span data-stu-id="462f0-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="462f0-107">Чтобы упростить этот переход, был разработан [набор средств для миграции с AzureRM на Az](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="462f0-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="462f0-108">Миграция всегда сопряжена со сложностями, и эта статья поможет вам начать переход на новый модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="462f0-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="462f0-109">Дополнительные сведения о том, для чего был создан модуль Az PowerShell, см. в статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="462f0-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="462f0-110">Полный список критических изменений между AzureRM и Az см. [здесь](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="462f0-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="462f0-111">Убедитесь, что существующие скрипты работают с последним выпуском AzureRM</span><span class="sxs-lookup"><span data-stu-id="462f0-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="462f0-112">Перед выполнением любых действий миграции проверьте, какие версии AzureRM установлены в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="462f0-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="462f0-113">Это позволит проверить, запущены ли скрипты с последним выпуском, и поможет узнать, какие версии AzureRM необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="462f0-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="462f0-114">Чтобы проверить установленные версии AzureRM, выполните приведенный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="462f0-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="462f0-115">**Последний** доступный выпуск AzureRM — **6.13.1** .</span><span class="sxs-lookup"><span data-stu-id="462f0-115">The **latest** available release of AzureRM is **6.13.1** .</span></span> <span data-ttu-id="462f0-116">Если у вас нет этой версии, возможно, ваши существующие скрипты нужно будет изменить для работы с модулем Az в дополнение к изменениям, описанным в этой статье и [списке критических изменений](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="462f0-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="462f0-117">Если скрипты не работают с AzureRM 6.13.1, обновите их в соответствии с [руководством по переходу AzureRM с версии 5.x на 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="462f0-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="462f0-118">Если вы используете более раннюю версию модуля AzureRM, найдите нужное руководство. Руководства по миграции существуют для каждого основного номера версии.</span><span class="sxs-lookup"><span data-stu-id="462f0-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="462f0-119">Установка набора средств для миграции с AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="462f0-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="462f0-120">Автоматический перенос скриптов PowerShell</span><span class="sxs-lookup"><span data-stu-id="462f0-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="462f0-121">Используя набор средств для миграции с AzureRM на Az, вы можете подготовить план, который определяет изменения, которые будут внесены в скрипты до их внесения и установки модуля Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="462f0-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="462f0-122">В статье [Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) показано, как выполнить автоматический перенос скриптов PowerShell из AzureRM в модуль Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="462f0-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="462f0-123">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="462f0-123">Next steps</span></span>

<span data-ttu-id="462f0-124">[Установка Azure PowerShell](install-az-ps.md)
[Удаление AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="462f0-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>