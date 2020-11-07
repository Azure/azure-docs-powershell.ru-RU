---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 99cf5e96e859932863236eacc1ad83a0b73ceecf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905250"
---
# <span data-ttu-id="b6595-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="b6595-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="b6595-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6595-102">SYNOPSIS</span></span>
<span data-ttu-id="b6595-103">Получение квоты использования подписки.</span><span class="sxs-lookup"><span data-stu-id="b6595-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="b6595-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6595-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6595-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6595-105">DESCRIPTION</span></span>
<span data-ttu-id="b6595-106">Получение квоты использования подписки.</span><span class="sxs-lookup"><span data-stu-id="b6595-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="b6595-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6595-107">EXAMPLES</span></span>

### <span data-ttu-id="b6595-108">Получение квоты использования путем ввода местоположения</span><span class="sxs-lookup"><span data-stu-id="b6595-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="b6595-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6595-109">PARAMETERS</span></span>

### <span data-ttu-id="b6595-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6595-110">-DefaultProfile</span></span>
<span data-ttu-id="b6595-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6595-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6595-112">-Location</span><span class="sxs-lookup"><span data-stu-id="b6595-112">-Location</span></span>
<span data-ttu-id="b6595-113">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="b6595-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="b6595-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6595-114">CommonParameters</span></span>
<span data-ttu-id="b6595-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6595-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6595-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6595-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6595-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6595-117">INPUTS</span></span>

### <span data-ttu-id="b6595-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="b6595-118">None</span></span>

## <span data-ttu-id="b6595-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6595-119">OUTPUTS</span></span>

### <span data-ttu-id="b6595-120">Microsoft. Azure. Commands. SignalR. Models. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="b6595-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="b6595-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6595-121">NOTES</span></span>

## <span data-ttu-id="b6595-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6595-122">RELATED LINKS</span></span>
