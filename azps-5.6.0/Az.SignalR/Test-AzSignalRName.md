---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955363"
---
# <span data-ttu-id="60e51-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="60e51-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="60e51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e51-102">SYNOPSIS</span></span>
<span data-ttu-id="60e51-103">Проверьте доступность имени.</span><span class="sxs-lookup"><span data-stu-id="60e51-103">Check the availability of a name.</span></span> <span data-ttu-id="60e51-104">Псевдоним: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="60e51-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="60e51-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60e51-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60e51-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e51-106">DESCRIPTION</span></span>
<span data-ttu-id="60e51-107">Проверьте доступность имени.</span><span class="sxs-lookup"><span data-stu-id="60e51-107">Check the availability of a name.</span></span> <span data-ttu-id="60e51-108">Псевдоним: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="60e51-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="60e51-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60e51-109">EXAMPLES</span></span>

### <span data-ttu-id="60e51-110">Проверьте, существует ли имя.</span><span class="sxs-lookup"><span data-stu-id="60e51-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="60e51-111">Проверьте неисчерченное имя.</span><span class="sxs-lookup"><span data-stu-id="60e51-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="60e51-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60e51-112">PARAMETERS</span></span>

### <span data-ttu-id="60e51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e51-113">-DefaultProfile</span></span>
<span data-ttu-id="60e51-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60e51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e51-115">-Location</span><span class="sxs-lookup"><span data-stu-id="60e51-115">-Location</span></span>
<span data-ttu-id="60e51-116">Расположение службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="60e51-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e51-117">-Name</span><span class="sxs-lookup"><span data-stu-id="60e51-117">-Name</span></span>
<span data-ttu-id="60e51-118">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="60e51-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="60e51-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e51-119">CommonParameters</span></span>
<span data-ttu-id="60e51-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e51-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e51-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60e51-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e51-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60e51-122">INPUTS</span></span>

### <span data-ttu-id="60e51-123">System.String</span><span class="sxs-lookup"><span data-stu-id="60e51-123">System.String</span></span>

## <span data-ttu-id="60e51-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60e51-124">OUTPUTS</span></span>

### <span data-ttu-id="60e51-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60e51-125">System.Boolean</span></span>

## <span data-ttu-id="60e51-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60e51-126">NOTES</span></span>

## <span data-ttu-id="60e51-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60e51-127">RELATED LINKS</span></span>
