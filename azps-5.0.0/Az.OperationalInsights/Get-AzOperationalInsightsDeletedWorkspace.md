---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248500"
---
# <span data-ttu-id="8c345-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c345-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="8c345-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c345-102">SYNOPSIS</span></span>
<span data-ttu-id="8c345-103">Список удаленных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="8c345-103">List deleted workspaces.</span></span>

## <span data-ttu-id="8c345-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c345-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c345-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c345-105">DESCRIPTION</span></span>
<span data-ttu-id="8c345-106">Список удаленных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="8c345-106">List deleted workspaces.</span></span>

## <span data-ttu-id="8c345-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c345-107">EXAMPLES</span></span>

### <span data-ttu-id="8c345-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c345-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="8c345-109">Список удаленных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="8c345-109">List deleted workspaces.</span></span>

## <span data-ttu-id="8c345-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c345-110">PARAMETERS</span></span>

### <span data-ttu-id="8c345-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c345-111">-DefaultProfile</span></span>
<span data-ttu-id="8c345-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c345-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c345-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c345-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c345-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c345-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c345-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c345-115">CommonParameters</span></span>
<span data-ttu-id="8c345-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c345-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c345-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c345-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c345-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c345-118">INPUTS</span></span>

### <span data-ttu-id="8c345-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8c345-119">System.String</span></span>

## <span data-ttu-id="8c345-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c345-120">OUTPUTS</span></span>

### <span data-ttu-id="8c345-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c345-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8c345-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c345-122">NOTES</span></span>

## <span data-ttu-id="8c345-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c345-123">RELATED LINKS</span></span>
