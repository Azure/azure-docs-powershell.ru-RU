---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 2cf7f548db74a7c7393fcd52bb7183c54f5f4e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001000"
---
# <span data-ttu-id="b382c-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="b382c-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="b382c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b382c-102">SYNOPSIS</span></span>
<span data-ttu-id="b382c-103">Получает общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b382c-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="b382c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b382c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b382c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b382c-105">DESCRIPTION</span></span>
<span data-ttu-id="b382c-106">Командлет **Get-AzOperationalInsightsWorkspaceSharedKey** перечисляет общие ключи рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b382c-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="b382c-107">Эти ключи используются для подключения агентов Рабочей статистики к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b382c-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="b382c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b382c-108">EXAMPLES</span></span>

### <span data-ttu-id="b382c-109">Пример 1. Общие ключи по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="b382c-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="b382c-110">Эта команда получает общие ключи для рабочей области MyWorkspace в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b382c-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b382c-111">Пример 2. Поимыка общих ключей с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="b382c-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="b382c-112">Эта команда получает рабочее пространство MyWorkspace с помощью командлета Get-AzOperationalInsightsWorkspace, а затем передает ее **командлету Get-AzOperationalInsightsWorkspaceSharedKey.**</span><span class="sxs-lookup"><span data-stu-id="b382c-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="b382c-113">Команда получает общие ключи для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b382c-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="b382c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b382c-114">PARAMETERS</span></span>

### <span data-ttu-id="b382c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b382c-115">-DefaultProfile</span></span>
<span data-ttu-id="b382c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b382c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b382c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b382c-117">-Name</span></span>
<span data-ttu-id="b382c-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b382c-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b382c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b382c-119">-ResourceGroupName</span></span>
<span data-ttu-id="b382c-120">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b382c-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b382c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b382c-121">CommonParameters</span></span>
<span data-ttu-id="b382c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b382c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b382c-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b382c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b382c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b382c-124">INPUTS</span></span>

### <span data-ttu-id="b382c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b382c-125">System.String</span></span>

## <span data-ttu-id="b382c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b382c-126">OUTPUTS</span></span>

### <span data-ttu-id="b382c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="b382c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="b382c-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b382c-128">NOTES</span></span>

## <span data-ttu-id="b382c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b382c-129">RELATED LINKS</span></span>

[<span data-ttu-id="b382c-130">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b382c-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="b382c-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b382c-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


