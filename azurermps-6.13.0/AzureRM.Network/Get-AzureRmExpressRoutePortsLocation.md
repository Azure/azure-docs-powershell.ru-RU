---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734622"
---
# <span data-ttu-id="afac3-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="afac3-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="afac3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="afac3-102">SYNOPSIS</span></span>
<span data-ttu-id="afac3-103">Возвращает расположение, в котором доступны ExpressRoutePort ресурсы.</span><span class="sxs-lookup"><span data-stu-id="afac3-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afac3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="afac3-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afac3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afac3-105">DESCRIPTION</span></span>
<span data-ttu-id="afac3-106">Командлет **Get-AzureRmExpressRoutePortsLocation** используется для извлечения расположений, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="afac3-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="afac3-107">В качестве входных данных для определенного местоположения командлет выводит сведения о расположении, например список доступных пропускной способности в этой папке.</span><span class="sxs-lookup"><span data-stu-id="afac3-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="afac3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="afac3-108">EXAMPLES</span></span>

### <span data-ttu-id="afac3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afac3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="afac3-110">Список расположений, в которых доступны ExpressRoutePort ресурсы.</span><span class="sxs-lookup"><span data-stu-id="afac3-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="afac3-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="afac3-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="afac3-112">Список ExpressRoutePort пропускной способности, доступных в местоположении $loc.</span><span class="sxs-lookup"><span data-stu-id="afac3-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="afac3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="afac3-113">PARAMETERS</span></span>

### <span data-ttu-id="afac3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afac3-114">-DefaultProfile</span></span>
<span data-ttu-id="afac3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afac3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afac3-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="afac3-116">-LocationName</span></span>
<span data-ttu-id="afac3-117">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="afac3-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afac3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afac3-118">CommonParameters</span></span>
<span data-ttu-id="afac3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="afac3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afac3-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afac3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afac3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="afac3-121">INPUTS</span></span>

### <span data-ttu-id="afac3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="afac3-122">System.String</span></span>

## <span data-ttu-id="afac3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afac3-123">OUTPUTS</span></span>

### <span data-ttu-id="afac3-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="afac3-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="afac3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="afac3-125">NOTES</span></span>

## <span data-ttu-id="afac3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afac3-126">RELATED LINKS</span></span>
