---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734011"
---
# <span data-ttu-id="f97d7-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f97d7-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="f97d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f97d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f97d7-103">Возвращает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f97d7-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f97d7-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f97d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f97d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f97d7-106">Командлет **Get-AzureRmRelayNamespace** получает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f97d7-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="f97d7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f97d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f97d7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f97d7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="f97d7-109">Возвращает описание указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f97d7-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="f97d7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f97d7-110">PARAMETERS</span></span>

### <span data-ttu-id="f97d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97d7-111">-DefaultProfile</span></span>
<span data-ttu-id="f97d7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f97d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97d7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f97d7-113">-Name</span></span>
<span data-ttu-id="f97d7-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f97d7-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="f97d7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f97d7-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97d7-117">CommonParameters</span></span>
<span data-ttu-id="f97d7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f97d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97d7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97d7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97d7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f97d7-120">INPUTS</span></span>

### <span data-ttu-id="f97d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="f97d7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f97d7-122">System.String</span></span>

### <span data-ttu-id="f97d7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f97d7-123">-Name</span></span>
 <span data-ttu-id="f97d7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f97d7-124">System.String</span></span>

## <span data-ttu-id="f97d7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f97d7-125">OUTPUTS</span></span>

### <span data-ttu-id="f97d7-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. RelayNamespaceAttributes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f97d7-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f97d7-127">ProvisioningState: CreatedAt 4/12/2017 12:38:47: UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-Relay1 Location: Западная часть US Tags: {[TAG1, Tag1Value]} идентификатор:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-servicebus-WestUS/providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 имя: TestNameSpace-Relay1 тип: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="f97d7-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="f97d7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f97d7-128">NOTES</span></span>

## <span data-ttu-id="f97d7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f97d7-129">RELATED LINKS</span></span>

