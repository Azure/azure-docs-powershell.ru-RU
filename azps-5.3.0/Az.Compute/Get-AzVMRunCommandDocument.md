---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519611"
---
# <span data-ttu-id="e785a-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e785a-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="e785a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e785a-102">SYNOPSIS</span></span>
<span data-ttu-id="e785a-103">Получить документ команд "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="e785a-103">Get a run command document.</span></span>

## <span data-ttu-id="e785a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e785a-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e785a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e785a-105">DESCRIPTION</span></span>
<span data-ttu-id="e785a-106">Получить документ команд "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="e785a-106">Get a run command document.</span></span>

## <span data-ttu-id="e785a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e785a-107">EXAMPLES</span></span>

### <span data-ttu-id="e785a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e785a-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e785a-109">Возвращает определенный документ командной команды run for 'RunPowerShellScript' на "westus".</span><span class="sxs-lookup"><span data-stu-id="e785a-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="e785a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e785a-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e785a-111">Список всех доступных команд запуска на "запад".</span><span class="sxs-lookup"><span data-stu-id="e785a-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e785a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e785a-112">PARAMETERS</span></span>

### <span data-ttu-id="e785a-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e785a-113">-CommandId</span></span>
<span data-ttu-id="e785a-114">ИД команды.</span><span class="sxs-lookup"><span data-stu-id="e785a-114">The command ID.</span></span>

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

### <span data-ttu-id="e785a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e785a-115">-DefaultProfile</span></span>
<span data-ttu-id="e785a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e785a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e785a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e785a-117">-Location</span></span>
<span data-ttu-id="e785a-118">Расположение, для которого запрашиваются команды запуска.</span><span class="sxs-lookup"><span data-stu-id="e785a-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="e785a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e785a-119">CommonParameters</span></span>
<span data-ttu-id="e785a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e785a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e785a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e785a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e785a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e785a-122">INPUTS</span></span>

### <span data-ttu-id="e785a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e785a-123">System.String</span></span>

## <span data-ttu-id="e785a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e785a-124">OUTPUTS</span></span>

### <span data-ttu-id="e785a-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e785a-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e785a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e785a-126">NOTES</span></span>

## <span data-ttu-id="e785a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e785a-127">RELATED LINKS</span></span>
