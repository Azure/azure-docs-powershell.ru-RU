---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732194"
---
# <span data-ttu-id="74d00-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="74d00-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="74d00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74d00-102">SYNOPSIS</span></span>
<span data-ttu-id="74d00-103">Получает описание пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74d00-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74d00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74d00-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74d00-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74d00-105">DESCRIPTION</span></span>
<span data-ttu-id="74d00-106">Командлет **Get-AzureRmServiceBusNamespace** получает описание для указанного пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74d00-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="74d00-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74d00-107">EXAMPLES</span></span>

### <span data-ttu-id="74d00-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74d00-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="74d00-109">Возвращает описание пространства имен для заданного служебной шины.</span><span class="sxs-lookup"><span data-stu-id="74d00-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="74d00-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74d00-110">PARAMETERS</span></span>

### <span data-ttu-id="74d00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d00-111">-DefaultProfile</span></span>
<span data-ttu-id="74d00-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74d00-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d00-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74d00-113">-Name</span></span>
<span data-ttu-id="74d00-114">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="74d00-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d00-115">-ResourceGroupName</span></span>
<span data-ttu-id="74d00-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74d00-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d00-117">CommonParameters</span></span>
<span data-ttu-id="74d00-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74d00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d00-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d00-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74d00-120">INPUTS</span></span>

### <span data-ttu-id="74d00-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="74d00-121">-ResourceGroup</span></span>
<span data-ttu-id="74d00-122">System. String</span><span class="sxs-lookup"><span data-stu-id="74d00-122">System.String</span></span>

### <span data-ttu-id="74d00-123">-+ +</span><span class="sxs-lookup"><span data-stu-id="74d00-123">-NamespaceName</span></span>
 <span data-ttu-id="74d00-124">System. String</span><span class="sxs-lookup"><span data-stu-id="74d00-124">System.String</span></span>

## <span data-ttu-id="74d00-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74d00-125">OUTPUTS</span></span>

### <span data-ttu-id="74d00-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="74d00-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="74d00-127">Name (имя): SB-Example1 ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location: Запад США SKU: имя: Стандартный, емкость: 1, уровень: Стандартный ProvisioningState: успешное состояние: активный CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ включено: true</span><span class="sxs-lookup"><span data-stu-id="74d00-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="74d00-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="74d00-128">NOTES</span></span>
## <span data-ttu-id="74d00-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74d00-129">RELATED LINKS</span></span>

## <span data-ttu-id="74d00-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74d00-130">RELATED LINKS</span></span>

