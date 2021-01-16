---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413996"
---
# <span data-ttu-id="de986-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="de986-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="de986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de986-102">SYNOPSIS</span></span>
<span data-ttu-id="de986-103">Удаляет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="de986-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="de986-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de986-104">SYNTAX</span></span>

### <span data-ttu-id="de986-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de986-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de986-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="de986-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de986-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de986-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de986-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de986-108">DESCRIPTION</span></span>
<span data-ttu-id="de986-109">Для удаления сборки из учетной записи интеграции удаляется ее из учетной записи **AzIntegrationAccountAssembly.**</span><span class="sxs-lookup"><span data-stu-id="de986-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="de986-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de986-110">EXAMPLES</span></span>

### <span data-ttu-id="de986-111">Пример 1. Удаление сборки по параметрам</span><span class="sxs-lookup"><span data-stu-id="de986-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="de986-112">Удаляет сборку sampleAssembly, расположенную в учетной записи интеграции sampleIntegrationAccount.</span><span class="sxs-lookup"><span data-stu-id="de986-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="de986-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de986-113">PARAMETERS</span></span>

### <span data-ttu-id="de986-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de986-114">-DefaultProfile</span></span>
<span data-ttu-id="de986-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de986-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de986-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de986-116">-InputObject</span></span>
<span data-ttu-id="de986-117">Сборка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="de986-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de986-118">-Name</span><span class="sxs-lookup"><span data-stu-id="de986-118">-Name</span></span>
<span data-ttu-id="de986-119">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="de986-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="de986-120">-ParentName</span></span>
<span data-ttu-id="de986-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="de986-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de986-122">-PassThru</span></span>
<span data-ttu-id="de986-123">Возвращает, была ли команда успешной.</span><span class="sxs-lookup"><span data-stu-id="de986-123">Return whether the command was successful or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de986-124">-ResourceGroupName</span></span>
<span data-ttu-id="de986-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de986-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de986-126">-ResourceId</span></span>
<span data-ttu-id="de986-127">ID ресурса сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="de986-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de986-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de986-128">-Confirm</span></span>
<span data-ttu-id="de986-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de986-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de986-130">-WhatIf</span></span>
<span data-ttu-id="de986-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de986-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de986-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="de986-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de986-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de986-133">CommonParameters</span></span>
<span data-ttu-id="de986-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de986-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de986-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de986-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de986-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de986-136">INPUTS</span></span>

### <span data-ttu-id="de986-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="de986-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="de986-138">System.String</span><span class="sxs-lookup"><span data-stu-id="de986-138">System.String</span></span>

## <span data-ttu-id="de986-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de986-139">OUTPUTS</span></span>

### <span data-ttu-id="de986-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de986-140">System.Boolean</span></span>

## <span data-ttu-id="de986-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de986-141">NOTES</span></span>

## <span data-ttu-id="de986-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de986-142">RELATED LINKS</span></span>
