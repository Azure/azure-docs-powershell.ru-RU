---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397668"
---
# <span data-ttu-id="2326d-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2326d-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2326d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2326d-102">SYNOPSIS</span></span>
<span data-ttu-id="2326d-103">Проверяет наличие рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2326d-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2326d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2326d-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2326d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2326d-105">DESCRIPTION</span></span>
<span data-ttu-id="2326d-106">Командлет **Test-AzSynapseWorkspace** проверяет наличие рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2326d-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2326d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2326d-107">EXAMPLES</span></span>

### <span data-ttu-id="2326d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2326d-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="2326d-109">Эта команда проверяет наличие рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2326d-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2326d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2326d-110">PARAMETERS</span></span>

### <span data-ttu-id="2326d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2326d-111">-DefaultProfile</span></span>
<span data-ttu-id="2326d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2326d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2326d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2326d-113">-Name</span></span>
<span data-ttu-id="2326d-114">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="2326d-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2326d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2326d-115">-ResourceGroupName</span></span>
<span data-ttu-id="2326d-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2326d-116">Resource group name.</span></span>

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

### <span data-ttu-id="2326d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2326d-117">CommonParameters</span></span>
<span data-ttu-id="2326d-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2326d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2326d-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2326d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2326d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2326d-120">INPUTS</span></span>

### <span data-ttu-id="2326d-121">Нет</span><span class="sxs-lookup"><span data-stu-id="2326d-121">None</span></span>

## <span data-ttu-id="2326d-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2326d-122">OUTPUTS</span></span>

### <span data-ttu-id="2326d-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="2326d-123">System.Object</span></span>
## <span data-ttu-id="2326d-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2326d-124">NOTES</span></span>

## <span data-ttu-id="2326d-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2326d-125">RELATED LINKS</span></span>
