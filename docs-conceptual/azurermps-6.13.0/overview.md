---
title: Общие сведения об Azure PowerShell | Документация Майкрософт
description: Общие сведения об Azure PowerShell со ссылками на установку и настройку.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4827b9be1dddb3cefcbbadbd0aed4298f45452e1
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523237"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="c0ba5-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ba5-103">Overview of Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="c0ba5-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ba5-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="c0ba5-105">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0ba5-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="c0ba5-106">Запускайте Azure PowerShell в браузере с помощью [Cloud Shell](/azure/cloud-shell/overview) либо [установите](install-azurerm-ps.md) его на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c0ba5-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="c0ba5-107">Прежде чем начать использовать эту среду, прочтите статью о [начале работы](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c0ba5-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="c0ba5-108">Сведения о последнем выпуске см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c0ba5-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="c0ba5-109">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c0ba5-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

- [<span data-ttu-id="c0ba5-110">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="c0ba5-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/linux/powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="c0ba5-111">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="c0ba5-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/windows/powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="c0ba5-112">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c0ba5-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="c0ba5-113">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="c0ba5-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="c0ba5-114">Изучение основ PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ba5-114">Learn PowerShell basics</span></span>

<span data-ttu-id="c0ba5-115">Если вы не знакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0ba5-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

- <span data-ttu-id="c0ba5-116">[Installing Windows PowerShell](/powershell/scripting/install/installing-powershell) (Установка Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="c0ba5-116">[Installing PowerShell](/powershell/scripting/install/installing-powershell)</span></span>
- [<span data-ttu-id="c0ba5-117">Учебные ресурсы для PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ba5-117">PowerShell learning resources</span></span>](/powershell/scripting/learn/more-powershell-learning)

<span data-ttu-id="c0ba5-118">Вы также можете посмотреть этот видеоролик: [Основы PowerShell. Часть 1. Начало работы с PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="c0ba5-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="c0ba5-119">Развитие навыков с помощью Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="c0ba5-119">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="c0ba5-120">Автоматизация задач Azure с помощью скриптов в PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ba5-120">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="c0ba5-121">Дополнительные интерактивные руководства…</span><span class="sxs-lookup"><span data-stu-id="c0ba5-121">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="c0ba5-122">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0ba5-122">Other Azure PowerShell modules</span></span>

- [<span data-ttu-id="c0ba5-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c0ba5-123">Azure Active Directory</span></span>](/powershell/module/activedirectory/)
- [<span data-ttu-id="c0ba5-124">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c0ba5-124">Azure Service Fabric</span></span>](/powershell/module/AzureRM.ServiceFabric/)
