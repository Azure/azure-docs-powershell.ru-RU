---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065257"
---
# <span data-ttu-id="0289c-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="0289c-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="0289c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0289c-102">SYNOPSIS</span></span>
<span data-ttu-id="0289c-103">Получение квоты использования подписки.</span><span class="sxs-lookup"><span data-stu-id="0289c-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="0289c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0289c-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0289c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0289c-105">DESCRIPTION</span></span>
<span data-ttu-id="0289c-106">Получение квоты использования подписки.</span><span class="sxs-lookup"><span data-stu-id="0289c-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="0289c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0289c-107">EXAMPLES</span></span>

### <span data-ttu-id="0289c-108">Получение квоты использования путем ввода местоположения</span><span class="sxs-lookup"><span data-stu-id="0289c-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="0289c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0289c-109">PARAMETERS</span></span>

### <span data-ttu-id="0289c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0289c-110">-DefaultProfile</span></span>
<span data-ttu-id="0289c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0289c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0289c-112">-Location</span><span class="sxs-lookup"><span data-stu-id="0289c-112">-Location</span></span>
<span data-ttu-id="0289c-113">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="0289c-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="0289c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0289c-114">CommonParameters</span></span>
<span data-ttu-id="0289c-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0289c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0289c-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0289c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0289c-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0289c-117">INPUTS</span></span>

### <span data-ttu-id="0289c-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="0289c-118">None</span></span>

## <span data-ttu-id="0289c-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0289c-119">OUTPUTS</span></span>

### <span data-ttu-id="0289c-120">Microsoft. Azure. Commands. SignalR. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="0289c-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="0289c-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="0289c-121">NOTES</span></span>

## <span data-ttu-id="0289c-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0289c-122">RELATED LINKS</span></span>
