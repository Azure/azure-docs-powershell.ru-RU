---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077625"
---
# <span data-ttu-id="597f1-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="597f1-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="597f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="597f1-102">SYNOPSIS</span></span>
<span data-ttu-id="597f1-103">Получает описание пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="597f1-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="597f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="597f1-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="597f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="597f1-105">DESCRIPTION</span></span>
<span data-ttu-id="597f1-106">Командлет **Get-AzServiceBusNamespace** получает описание для указанного пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="597f1-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="597f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="597f1-107">EXAMPLES</span></span>

### <span data-ttu-id="597f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="597f1-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="597f1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="597f1-109">PARAMETERS</span></span>

### <span data-ttu-id="597f1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597f1-110">-DefaultProfile</span></span>
<span data-ttu-id="597f1-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="597f1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597f1-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="597f1-112">-Name</span></span>
<span data-ttu-id="597f1-113">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="597f1-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597f1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597f1-114">-ResourceGroupName</span></span>
<span data-ttu-id="597f1-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="597f1-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="597f1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597f1-116">CommonParameters</span></span>
<span data-ttu-id="597f1-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="597f1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597f1-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597f1-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597f1-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="597f1-119">INPUTS</span></span>

### <span data-ttu-id="597f1-120">System. String</span><span class="sxs-lookup"><span data-stu-id="597f1-120">System.String</span></span>

## <span data-ttu-id="597f1-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="597f1-121">OUTPUTS</span></span>

### <span data-ttu-id="597f1-122">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="597f1-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="597f1-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="597f1-123">NOTES</span></span>

## <span data-ttu-id="597f1-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="597f1-124">RELATED LINKS</span></span>
