---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312623"
---
# <span data-ttu-id="89e9b-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="89e9b-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="89e9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="89e9b-103">Обновляет шаг.</span><span class="sxs-lookup"><span data-stu-id="89e9b-103">Updates the step.</span></span>

## <span data-ttu-id="89e9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89e9b-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="89e9b-106">Командлет **Set-AzDeploymentManagerStep** обновляет шаг с указанным объектом Step.</span><span class="sxs-lookup"><span data-stu-id="89e9b-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="89e9b-107">Командлет возвращает обновленный объект шага.</span><span class="sxs-lookup"><span data-stu-id="89e9b-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="89e9b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89e9b-108">EXAMPLES</span></span>

### <span data-ttu-id="89e9b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89e9b-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="89e9b-110">Эта команда обновляет шаг, с именем и свойством ResourceGroup которого совпадают свойства Name и ResourceGroupName для $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="89e9b-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="89e9b-111">Шаг будет обновлен до свойств, заданных в $stepObject.</span><span class="sxs-lookup"><span data-stu-id="89e9b-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="89e9b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89e9b-112">PARAMETERS</span></span>

### <span data-ttu-id="89e9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e9b-113">-DefaultProfile</span></span>
<span data-ttu-id="89e9b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89e9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89e9b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89e9b-115">-InputObject</span></span>
<span data-ttu-id="89e9b-116">Объект Step.</span><span class="sxs-lookup"><span data-stu-id="89e9b-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e9b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89e9b-117">-Confirm</span></span>
<span data-ttu-id="89e9b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89e9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e9b-119">-WhatIf</span></span>
<span data-ttu-id="89e9b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89e9b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e9b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89e9b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e9b-122">CommonParameters</span></span>
<span data-ttu-id="89e9b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89e9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e9b-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89e9b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e9b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89e9b-125">INPUTS</span></span>

### <span data-ttu-id="89e9b-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="89e9b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="89e9b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e9b-127">OUTPUTS</span></span>

### <span data-ttu-id="89e9b-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="89e9b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="89e9b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="89e9b-129">NOTES</span></span>

## <span data-ttu-id="89e9b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89e9b-130">RELATED LINKS</span></span>
