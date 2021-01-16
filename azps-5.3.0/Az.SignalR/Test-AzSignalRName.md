---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506685"
---
# <span data-ttu-id="307e5-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="307e5-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="307e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="307e5-102">SYNOPSIS</span></span>
<span data-ttu-id="307e5-103">Проверьте доступность имени.</span><span class="sxs-lookup"><span data-stu-id="307e5-103">Check the availability of a name.</span></span> <span data-ttu-id="307e5-104">Псевдоним: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="307e5-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="307e5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="307e5-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="307e5-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="307e5-106">DESCRIPTION</span></span>
<span data-ttu-id="307e5-107">Проверьте доступность имени.</span><span class="sxs-lookup"><span data-stu-id="307e5-107">Check the availability of a name.</span></span> <span data-ttu-id="307e5-108">Псевдоним: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="307e5-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="307e5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="307e5-109">EXAMPLES</span></span>

### <span data-ttu-id="307e5-110">Проверьте, существует ли имя.</span><span class="sxs-lookup"><span data-stu-id="307e5-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="307e5-111">Проверьте неисчерченное имя.</span><span class="sxs-lookup"><span data-stu-id="307e5-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="307e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="307e5-112">PARAMETERS</span></span>

### <span data-ttu-id="307e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307e5-113">-DefaultProfile</span></span>
<span data-ttu-id="307e5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="307e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="307e5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="307e5-115">-Location</span></span>
<span data-ttu-id="307e5-116">Расположение службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="307e5-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="307e5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="307e5-117">-Name</span></span>
<span data-ttu-id="307e5-118">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="307e5-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="307e5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307e5-119">CommonParameters</span></span>
<span data-ttu-id="307e5-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307e5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307e5-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="307e5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307e5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="307e5-122">INPUTS</span></span>

### <span data-ttu-id="307e5-123">System.String</span><span class="sxs-lookup"><span data-stu-id="307e5-123">System.String</span></span>

## <span data-ttu-id="307e5-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="307e5-124">OUTPUTS</span></span>

### <span data-ttu-id="307e5-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="307e5-125">System.Boolean</span></span>

## <span data-ttu-id="307e5-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="307e5-126">NOTES</span></span>

## <span data-ttu-id="307e5-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="307e5-127">RELATED LINKS</span></span>
