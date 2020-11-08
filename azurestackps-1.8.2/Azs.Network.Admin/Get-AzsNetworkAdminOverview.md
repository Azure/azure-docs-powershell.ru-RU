---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076615"
---
# <span data-ttu-id="5b73c-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="5b73c-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="5b73c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b73c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b73c-103">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b73c-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="5b73c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b73c-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="5b73c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b73c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b73c-106">Получите общие сведения о состоянии поставщика сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b73c-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="5b73c-107">Отдельные свойства предоставляют подробные сведения об использовании ресурсов и работоспособности компонента.</span><span class="sxs-lookup"><span data-stu-id="5b73c-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="5b73c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b73c-108">EXAMPLES</span></span>

### <span data-ttu-id="5b73c-109">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="5b73c-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="5b73c-110">Общие сведения об администраторе сети.</span><span class="sxs-lookup"><span data-stu-id="5b73c-110">Get network admin overview.</span></span>

### <span data-ttu-id="5b73c-111">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="5b73c-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="5b73c-112">Получение сведений об использовании общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5b73c-112">Get public ip address usage.</span></span>

## <span data-ttu-id="5b73c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b73c-113">PARAMETERS</span></span>

### <span data-ttu-id="5b73c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b73c-114">CommonParameters</span></span>
<span data-ttu-id="5b73c-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b73c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b73c-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b73c-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b73c-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b73c-117">INPUTS</span></span>

## <span data-ttu-id="5b73c-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b73c-118">OUTPUTS</span></span>

### <span data-ttu-id="5b73c-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="5b73c-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="5b73c-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b73c-120">NOTES</span></span>

## <span data-ttu-id="5b73c-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b73c-121">RELATED LINKS</span></span>
