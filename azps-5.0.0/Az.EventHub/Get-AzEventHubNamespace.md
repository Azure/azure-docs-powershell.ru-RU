---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248684"
---
# <span data-ttu-id="0d14c-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0d14c-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="0d14c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d14c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d14c-103">Получает сведения о пространстве имен концентраторов событий или получает список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="0d14c-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="0d14c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d14c-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d14c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d14c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d14c-106">Командлет Get-AzEventHubNamespace получает либо сведения о заданном пространстве имен концентраторов событий, либо список всех пространств имен концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="0d14c-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="0d14c-107">Если указано имя пространства имен, возвращается информация об одном пространстве имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="0d14c-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="0d14c-108">Если имя пространства имен не указано, возвращается список пространств имен.</span><span class="sxs-lookup"><span data-stu-id="0d14c-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="0d14c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d14c-109">EXAMPLES</span></span>

### <span data-ttu-id="0d14c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d14c-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="0d14c-111">Получает сведения о MyNamespaceName пространства \` имен \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0d14c-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0d14c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d14c-112">PARAMETERS</span></span>

### <span data-ttu-id="0d14c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d14c-113">-DefaultProfile</span></span>
<span data-ttu-id="0d14c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d14c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d14c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d14c-115">-Name</span></span>
<span data-ttu-id="0d14c-116">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="0d14c-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="0d14c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d14c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d14c-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0d14c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0d14c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d14c-119">CommonParameters</span></span>
<span data-ttu-id="0d14c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d14c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d14c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d14c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d14c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d14c-122">INPUTS</span></span>

### <span data-ttu-id="0d14c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0d14c-123">System.String</span></span>

## <span data-ttu-id="0d14c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d14c-124">OUTPUTS</span></span>

### <span data-ttu-id="0d14c-125">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0d14c-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0d14c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d14c-126">NOTES</span></span>

## <span data-ttu-id="0d14c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d14c-127">RELATED LINKS</span></span>
