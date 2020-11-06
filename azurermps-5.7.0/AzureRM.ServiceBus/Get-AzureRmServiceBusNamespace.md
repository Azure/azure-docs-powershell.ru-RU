---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561476"
---
# <span data-ttu-id="16910-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="16910-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="16910-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16910-102">SYNOPSIS</span></span>
<span data-ttu-id="16910-103">Получает описание пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16910-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16910-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16910-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16910-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16910-105">DESCRIPTION</span></span>
<span data-ttu-id="16910-106">Командлет **Get-AzureRmServiceBusNamespace** получает описание для указанного пространства имен служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16910-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="16910-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16910-107">EXAMPLES</span></span>

### <span data-ttu-id="16910-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16910-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="16910-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16910-109">PARAMETERS</span></span>

### <span data-ttu-id="16910-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16910-110">-DefaultProfile</span></span>
<span data-ttu-id="16910-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16910-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16910-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16910-112">-Name</span></span>
<span data-ttu-id="16910-113">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="16910-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16910-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16910-114">-ResourceGroupName</span></span>
<span data-ttu-id="16910-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16910-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16910-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16910-116">CommonParameters</span></span>
<span data-ttu-id="16910-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16910-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16910-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16910-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16910-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16910-119">INPUTS</span></span>

### <span data-ttu-id="16910-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16910-120">-ResourceGroup</span></span>
<span data-ttu-id="16910-121">System. String</span><span class="sxs-lookup"><span data-stu-id="16910-121">System.String</span></span>

### <span data-ttu-id="16910-122">-+ +</span><span class="sxs-lookup"><span data-stu-id="16910-122">-NamespaceName</span></span>
 <span data-ttu-id="16910-123">System. String</span><span class="sxs-lookup"><span data-stu-id="16910-123">System.String</span></span>

## <span data-ttu-id="16910-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16910-124">OUTPUTS</span></span>

### <span data-ttu-id="16910-125">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="16910-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="16910-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="16910-126">NOTES</span></span>

## <span data-ttu-id="16910-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16910-127">RELATED LINKS</span></span>

