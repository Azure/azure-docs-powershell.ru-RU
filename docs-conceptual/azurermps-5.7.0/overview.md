---
title: Общие сведения об Azure PowerShell | Документация Майкрософт
description: Общие сведения об Azure PowerShell со ссылками на установку и настройку.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: e5c344ca59de37eeb59bba538e7437d4a0c26ed7
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736415"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="0c644-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c644-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="0c644-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="0c644-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="0c644-105">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c644-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="0c644-106">Запускайте Azure PowerShell в браузере с помощью [Cloud Shell](/azure/cloud-shell/overview) либо [установите](install-azurerm-ps.md) его на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0c644-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="0c644-107">Прежде чем начать использовать эту среду, прочтите статью о [начале работы](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0c644-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="0c644-108">Сведения о последнем выпуске см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0c644-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="0c644-109">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0c644-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="0c644-110">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="0c644-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="0c644-111">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="0c644-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="0c644-112">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="0c644-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="0c644-113">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="0c644-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="0c644-114">Изучение основ PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c644-114">Learn PowerShell basics</span></span>

<span data-ttu-id="0c644-115">Если вы не знакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c644-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* <span data-ttu-id="0c644-116">[Installing Windows PowerShell](/powershell/scripting/installing-windows-powershell) (Установка Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="0c644-116">[Installing PowerShell](/powershell/scripting/installing-windows-powershell)</span></span>
* <span data-ttu-id="0c644-117">[Scripting with Windows PowerShell](/powershell/scripting/scripting-with-windows-powershell) (Написание скриптов с помощью Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="0c644-117">[Scripting with PowerShell](/powershell/scripting/scripting-with-windows-powershell)</span></span>

<span data-ttu-id="0c644-118">Вы также можете посмотреть этот видеоролик: [Основы PowerShell. Часть 1. Начало работы с PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="0c644-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="0c644-119">Или пройдите [краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="0c644-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="0c644-120">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c644-120">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="0c644-121">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0c644-121">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="0c644-122">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="0c644-122">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="0c644-123">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0c644-123">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="0c644-124">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="0c644-124">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
