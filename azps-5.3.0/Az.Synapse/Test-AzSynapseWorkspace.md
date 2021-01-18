---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507049"
---
# <span data-ttu-id="7ee6a-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7ee6a-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="7ee6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee6a-103">Проверяет наличие рабочей области synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7ee6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ee6a-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ee6a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ee6a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ee6a-106">Командлет **Test-AzSynapseWorkspace** проверяет наличие рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7ee6a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ee6a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ee6a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ee6a-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="7ee6a-109">Эта команда проверяет наличие рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="7ee6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ee6a-110">PARAMETERS</span></span>

### <span data-ttu-id="7ee6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee6a-111">-DefaultProfile</span></span>
<span data-ttu-id="7ee6a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee6a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7ee6a-113">-Name</span></span>
<span data-ttu-id="7ee6a-114">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7ee6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ee6a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee6a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee6a-117">CommonParameters</span></span>
<span data-ttu-id="7ee6a-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee6a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee6a-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ee6a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee6a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ee6a-120">INPUTS</span></span>

### <span data-ttu-id="7ee6a-121">Нет</span><span class="sxs-lookup"><span data-stu-id="7ee6a-121">None</span></span>

## <span data-ttu-id="7ee6a-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ee6a-122">OUTPUTS</span></span>

### <span data-ttu-id="7ee6a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="7ee6a-123">System.Object</span></span>
## <span data-ttu-id="7ee6a-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ee6a-124">NOTES</span></span>

## <span data-ttu-id="7ee6a-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ee6a-125">RELATED LINKS</span></span>
