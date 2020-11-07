---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912672"
---
# <span data-ttu-id="c0a86-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c0a86-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="c0a86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0a86-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a86-103">Возвращает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0a86-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c0a86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0a86-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0a86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a86-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a86-106">Командлет **Get-AzRelayNamespace** получает описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0a86-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c0a86-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0a86-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a86-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0a86-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

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

<span data-ttu-id="c0a86-109">Возвращает описание указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="c0a86-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="c0a86-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0a86-110">PARAMETERS</span></span>

### <span data-ttu-id="c0a86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a86-111">-DefaultProfile</span></span>
<span data-ttu-id="c0a86-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a86-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0a86-113">-Name</span></span>
<span data-ttu-id="c0a86-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="c0a86-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c0a86-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a86-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0a86-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0a86-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="c0a86-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a86-117">CommonParameters</span></span>
<span data-ttu-id="c0a86-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0a86-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a86-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a86-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a86-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0a86-120">INPUTS</span></span>

### <span data-ttu-id="c0a86-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a86-121">System.String</span></span>

## <span data-ttu-id="c0a86-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a86-122">OUTPUTS</span></span>

### <span data-ttu-id="c0a86-123">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c0a86-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="c0a86-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0a86-124">NOTES</span></span>

## <span data-ttu-id="c0a86-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0a86-125">RELATED LINKS</span></span>
