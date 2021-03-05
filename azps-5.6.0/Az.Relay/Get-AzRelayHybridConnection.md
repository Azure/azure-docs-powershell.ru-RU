---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 9e7edf3a7aa076d7bb5ad4b1a36aecdedfd89b92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000632"
---
# <span data-ttu-id="3e6a0-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e6a0-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="3e6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6a0-103">Возвращает описание указанного гибридного подключения в области имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3e6a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e6a0-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6a0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6a0-106">Командлет **Get-AzRelayHybridConnection** получает описание указанного гибридного подключения в области имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3e6a0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e6a0-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6a0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e6a0-108">Example 1</span></span>
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

<span data-ttu-id="3e6a0-109">Возвращает описание HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="3e6a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e6a0-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6a0-111">-DefaultProfile</span></span>
<span data-ttu-id="3e6a0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6a0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3e6a0-113">-Name</span></span>
<span data-ttu-id="3e6a0-114">Имя HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="3e6a0-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3e6a0-115">-Namespace</span></span>
<span data-ttu-id="3e6a0-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-116">Namespace Name.</span></span>

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

### <span data-ttu-id="3e6a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e6a0-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e6a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6a0-119">CommonParameters</span></span>
<span data-ttu-id="3e6a0-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6a0-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6a0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6a0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e6a0-122">INPUTS</span></span>

### <span data-ttu-id="3e6a0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3e6a0-123">System.String</span></span>

## <span data-ttu-id="3e6a0-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e6a0-124">OUTPUTS</span></span>

### <span data-ttu-id="3e6a0-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="3e6a0-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="3e6a0-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e6a0-126">NOTES</span></span>

## <span data-ttu-id="3e6a0-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e6a0-127">RELATED LINKS</span></span>
