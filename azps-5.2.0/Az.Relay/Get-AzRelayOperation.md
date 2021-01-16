---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395031"
---
# <span data-ttu-id="a3bec-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="a3bec-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="a3bec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3bec-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bec-103">Список поддерживаемых операций ретрансляции</span><span class="sxs-lookup"><span data-stu-id="a3bec-103">List supported Relay Operations</span></span>

## <span data-ttu-id="a3bec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3bec-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3bec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3bec-105">DESCRIPTION</span></span>
<span data-ttu-id="a3bec-106">Командлет **Get-AzRelayOperation** перечисляет поддерживаемые ретранслятором операции.</span><span class="sxs-lookup"><span data-stu-id="a3bec-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="a3bec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3bec-107">EXAMPLES</span></span>

### <span data-ttu-id="a3bec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3bec-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="a3bec-109">Списки операций, поддерживаемых ретранслятором</span><span class="sxs-lookup"><span data-stu-id="a3bec-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="a3bec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3bec-110">PARAMETERS</span></span>

### <span data-ttu-id="a3bec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bec-111">-DefaultProfile</span></span>
<span data-ttu-id="a3bec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3bec-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bec-113">CommonParameters</span></span>
<span data-ttu-id="a3bec-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bec-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bec-115">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3bec-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bec-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3bec-116">INPUTS</span></span>

### <span data-ttu-id="a3bec-117">Нет</span><span class="sxs-lookup"><span data-stu-id="a3bec-117">None</span></span>

## <span data-ttu-id="a3bec-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3bec-118">OUTPUTS</span></span>

### <span data-ttu-id="a3bec-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="a3bec-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="a3bec-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3bec-120">NOTES</span></span>

## <span data-ttu-id="a3bec-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3bec-121">RELATED LINKS</span></span>
