---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 7dab3fd72dcd7ac097dbf5a1d5da342c39d3c504
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905705"
---
# <span data-ttu-id="df1f1-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="df1f1-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="df1f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="df1f1-103">Возвращает описание указанного HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="df1f1-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="df1f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df1f1-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df1f1-105">DESCRIPTION</span></span>
<span data-ttu-id="df1f1-106">Командлет **Get-AzRelayHybridConnection** Возвращает описание указанной HybridConnection в пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="df1f1-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="df1f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df1f1-107">EXAMPLES</span></span>

### <span data-ttu-id="df1f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df1f1-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="df1f1-109">Возвращает описание HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="df1f1-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="df1f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df1f1-110">PARAMETERS</span></span>

### <span data-ttu-id="df1f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1f1-111">-DefaultProfile</span></span>
<span data-ttu-id="df1f1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df1f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1f1-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df1f1-113">-Name</span></span>
<span data-ttu-id="df1f1-114">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="df1f1-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="df1f1-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df1f1-115">-Namespace</span></span>
<span data-ttu-id="df1f1-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="df1f1-116">Namespace Name.</span></span>

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

### <span data-ttu-id="df1f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="df1f1-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df1f1-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="df1f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1f1-119">CommonParameters</span></span>
<span data-ttu-id="df1f1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df1f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1f1-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1f1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1f1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df1f1-122">INPUTS</span></span>

### <span data-ttu-id="df1f1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="df1f1-123">System.String</span></span>

## <span data-ttu-id="df1f1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df1f1-124">OUTPUTS</span></span>

### <span data-ttu-id="df1f1-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="df1f1-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="df1f1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="df1f1-126">NOTES</span></span>

## <span data-ttu-id="df1f1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df1f1-127">RELATED LINKS</span></span>
