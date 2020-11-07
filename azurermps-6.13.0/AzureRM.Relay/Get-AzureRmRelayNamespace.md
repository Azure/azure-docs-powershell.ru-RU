---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 05482dfae5cf4e68a82763253d0b4507b0fe364c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732458"
---
# <span data-ttu-id="bced1-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="bced1-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="bced1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bced1-102">SYNOPSIS</span></span>
<span data-ttu-id="bced1-103">Возвращает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bced1-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bced1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bced1-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bced1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bced1-105">DESCRIPTION</span></span>
<span data-ttu-id="bced1-106">Командлет **Get-AzureRmRelayNamespace** получает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bced1-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="bced1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bced1-107">EXAMPLES</span></span>

### <span data-ttu-id="bced1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bced1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="bced1-109">Возвращает описание указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="bced1-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="bced1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bced1-110">PARAMETERS</span></span>

### <span data-ttu-id="bced1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bced1-111">-DefaultProfile</span></span>
<span data-ttu-id="bced1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bced1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bced1-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bced1-113">-Name</span></span>
<span data-ttu-id="bced1-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="bced1-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bced1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bced1-115">-ResourceGroupName</span></span>
<span data-ttu-id="bced1-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bced1-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bced1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bced1-117">CommonParameters</span></span>
<span data-ttu-id="bced1-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bced1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bced1-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bced1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bced1-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bced1-120">INPUTS</span></span>

### <span data-ttu-id="bced1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bced1-121">System.String</span></span>


## <span data-ttu-id="bced1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bced1-122">OUTPUTS</span></span>

### <span data-ttu-id="bced1-123">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bced1-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="bced1-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="bced1-124">NOTES</span></span>

## <span data-ttu-id="bced1-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bced1-125">RELATED LINKS</span></span>
