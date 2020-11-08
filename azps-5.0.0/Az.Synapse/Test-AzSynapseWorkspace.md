---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245142"
---
# <span data-ttu-id="e7fb8-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7fb8-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e7fb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fb8-103">Проверка существования рабочей области аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e7fb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7fb8-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7fb8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fb8-106">Командлет **Test-AzSynapseWorkspace** проверяет наличие рабочей области для аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e7fb8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="e7fb8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7fb8-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="e7fb8-109">Эта команда проверяет наличие рабочей области Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e7fb8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="e7fb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fb8-111">-DefaultProfile</span></span>
<span data-ttu-id="e7fb8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7fb8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7fb8-113">-Name</span></span>
<span data-ttu-id="e7fb8-114">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e7fb8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fb8-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7fb8-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-116">Resource group name.</span></span>

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

### <span data-ttu-id="e7fb8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fb8-117">CommonParameters</span></span>
<span data-ttu-id="e7fb8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7fb8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fb8-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7fb8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fb8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7fb8-120">INPUTS</span></span>

### <span data-ttu-id="e7fb8-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="e7fb8-121">None</span></span>

## <span data-ttu-id="e7fb8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7fb8-122">OUTPUTS</span></span>

### <span data-ttu-id="e7fb8-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="e7fb8-123">System.Object</span></span>
## <span data-ttu-id="e7fb8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7fb8-124">NOTES</span></span>

## <span data-ttu-id="e7fb8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7fb8-125">RELATED LINKS</span></span>
