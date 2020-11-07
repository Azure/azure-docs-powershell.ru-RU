---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902418"
---
# <span data-ttu-id="3559e-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="3559e-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="3559e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3559e-102">SYNOPSIS</span></span>
<span data-ttu-id="3559e-103">Возвращает расположение, в котором доступны ExpressRoutePort ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3559e-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="3559e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3559e-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3559e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3559e-105">DESCRIPTION</span></span>
<span data-ttu-id="3559e-106">Командлет **Get-AzExpressRoutePortsLocation** используется для извлечения расположений, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3559e-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="3559e-107">В качестве входных данных для определенного местоположения командлет выводит сведения о расположении, например список доступных пропускной способности в этой папке.</span><span class="sxs-lookup"><span data-stu-id="3559e-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="3559e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3559e-108">EXAMPLES</span></span>

### <span data-ttu-id="3559e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3559e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="3559e-110">Список расположений, в которых доступны ExpressRoutePort ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3559e-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="3559e-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3559e-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="3559e-112">Список ExpressRoutePort пропускной способности, доступных в местоположении $loc.</span><span class="sxs-lookup"><span data-stu-id="3559e-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="3559e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3559e-113">PARAMETERS</span></span>

### <span data-ttu-id="3559e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3559e-114">-DefaultProfile</span></span>
<span data-ttu-id="3559e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3559e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3559e-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="3559e-116">-LocationName</span></span>
<span data-ttu-id="3559e-117">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="3559e-117">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3559e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3559e-118">CommonParameters</span></span>
<span data-ttu-id="3559e-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3559e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3559e-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3559e-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3559e-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3559e-121">INPUTS</span></span>

### <span data-ttu-id="3559e-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3559e-122">System.String</span></span>

## <span data-ttu-id="3559e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3559e-123">OUTPUTS</span></span>

### <span data-ttu-id="3559e-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="3559e-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="3559e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3559e-125">NOTES</span></span>

## <span data-ttu-id="3559e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3559e-126">RELATED LINKS</span></span>
