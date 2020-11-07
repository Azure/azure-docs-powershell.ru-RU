---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 546dbdfe2de2a87c0ce2887c83139a527ecf769c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905701"
---
# <span data-ttu-id="82b40-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="82b40-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="82b40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82b40-102">SYNOPSIS</span></span>
<span data-ttu-id="82b40-103">Возвращает описание для указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="82b40-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="82b40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82b40-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b40-105">DESCRIPTION</span></span>
<span data-ttu-id="82b40-106">Командлет **Get-AzWcfRelay** Возвращает описание указанного WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="82b40-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="82b40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82b40-107">EXAMPLES</span></span>

### <span data-ttu-id="82b40-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82b40-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="82b40-109">Возвращает описание WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="82b40-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="82b40-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82b40-110">PARAMETERS</span></span>

### <span data-ttu-id="82b40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b40-111">-DefaultProfile</span></span>
<span data-ttu-id="82b40-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82b40-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b40-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82b40-113">-Name</span></span>
<span data-ttu-id="82b40-114">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="82b40-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b40-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="82b40-115">-Namespace</span></span>
<span data-ttu-id="82b40-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="82b40-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b40-117">-ResourceGroupName</span></span>
<span data-ttu-id="82b40-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82b40-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b40-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b40-119">CommonParameters</span></span>
<span data-ttu-id="82b40-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82b40-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b40-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b40-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b40-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82b40-122">INPUTS</span></span>

### <span data-ttu-id="82b40-123">System. String</span><span class="sxs-lookup"><span data-stu-id="82b40-123">System.String</span></span>

## <span data-ttu-id="82b40-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b40-124">OUTPUTS</span></span>

### <span data-ttu-id="82b40-125">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="82b40-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="82b40-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="82b40-126">NOTES</span></span>

## <span data-ttu-id="82b40-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82b40-127">RELATED LINKS</span></span>
