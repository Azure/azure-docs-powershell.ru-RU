---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555579"
---
# <span data-ttu-id="39c41-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="39c41-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="39c41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39c41-102">SYNOPSIS</span></span>
<span data-ttu-id="39c41-103">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39c41-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="39c41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39c41-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="39c41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c41-105">DESCRIPTION</span></span>
<span data-ttu-id="39c41-106">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39c41-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="39c41-107">Отдельные свойства предоставляют подробные сведения об использовании ресурсов и работоспособности компонента.</span><span class="sxs-lookup"><span data-stu-id="39c41-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="39c41-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39c41-108">EXAMPLES</span></span>

### <span data-ttu-id="39c41-109">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39c41-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="39c41-110">Общие сведения об администраторе сети.</span><span class="sxs-lookup"><span data-stu-id="39c41-110">Get network admin overview.</span></span>

### <span data-ttu-id="39c41-111">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="39c41-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="39c41-112">Получение сведений об использовании общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="39c41-112">Get public ip address usage.</span></span>

## <span data-ttu-id="39c41-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39c41-113">PARAMETERS</span></span>

### <span data-ttu-id="39c41-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c41-114">CommonParameters</span></span>
<span data-ttu-id="39c41-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39c41-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c41-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c41-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c41-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39c41-117">INPUTS</span></span>

## <span data-ttu-id="39c41-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c41-118">OUTPUTS</span></span>

### <span data-ttu-id="39c41-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="39c41-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="39c41-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="39c41-120">NOTES</span></span>

## <span data-ttu-id="39c41-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39c41-121">RELATED LINKS</span></span>

