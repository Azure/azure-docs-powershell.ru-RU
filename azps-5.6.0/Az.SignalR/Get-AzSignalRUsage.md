---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955491"
---
# <span data-ttu-id="ac4a3-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="ac4a3-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="ac4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4a3-103">Получите квоту использования подписки.</span><span class="sxs-lookup"><span data-stu-id="ac4a3-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="ac4a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac4a3-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac4a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ac4a3-106">Получите квоту использования подписки.</span><span class="sxs-lookup"><span data-stu-id="ac4a3-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="ac4a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="ac4a3-108">Получить квоту использования путем ввода данных о расположении</span><span class="sxs-lookup"><span data-stu-id="ac4a3-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="ac4a3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac4a3-109">PARAMETERS</span></span>

### <span data-ttu-id="ac4a3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4a3-110">-DefaultProfile</span></span>
<span data-ttu-id="ac4a3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4a3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac4a3-112">-Location</span><span class="sxs-lookup"><span data-stu-id="ac4a3-112">-Location</span></span>
<span data-ttu-id="ac4a3-113">Расположение службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ac4a3-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac4a3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4a3-114">CommonParameters</span></span>
<span data-ttu-id="ac4a3-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4a3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4a3-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac4a3-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4a3-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac4a3-117">INPUTS</span></span>

### <span data-ttu-id="ac4a3-118">Нет</span><span class="sxs-lookup"><span data-stu-id="ac4a3-118">None</span></span>

## <span data-ttu-id="ac4a3-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac4a3-119">OUTPUTS</span></span>

### <span data-ttu-id="ac4a3-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="ac4a3-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="ac4a3-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac4a3-121">NOTES</span></span>

## <span data-ttu-id="ac4a3-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac4a3-122">RELATED LINKS</span></span>
