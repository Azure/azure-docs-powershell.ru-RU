---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555740"
---
# <span data-ttu-id="a5b35-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a5b35-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="a5b35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5b35-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b35-103">Обновляет шаг.</span><span class="sxs-lookup"><span data-stu-id="a5b35-103">Updates a step.</span></span>

## <span data-ttu-id="a5b35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5b35-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b35-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b35-106">Командлет **Set-AzureRmDeploymentManagerStep** обновляет шаг с указанным объектом Step.</span><span class="sxs-lookup"><span data-stu-id="a5b35-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="a5b35-107">Командлет возвращает обновленный объект шага.</span><span class="sxs-lookup"><span data-stu-id="a5b35-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="a5b35-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b35-108">EXAMPLES</span></span>

### <span data-ttu-id="a5b35-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5b35-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="a5b35-110">Эта команда обновляет шаг, с именем и свойством ResourceGroup которого совпадают свойства Name и ResourceGroupName для $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="a5b35-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="a5b35-111">Шаг будет обновлен до свойств, заданных в $stepObject.</span><span class="sxs-lookup"><span data-stu-id="a5b35-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="a5b35-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b35-112">PARAMETERS</span></span>

### <span data-ttu-id="a5b35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b35-113">-DefaultProfile</span></span>
<span data-ttu-id="a5b35-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b35-115">-Шаг</span><span class="sxs-lookup"><span data-stu-id="a5b35-115">-Step</span></span>
<span data-ttu-id="a5b35-116">Объект Step.</span><span class="sxs-lookup"><span data-stu-id="a5b35-116">The step object.</span></span>

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

### <span data-ttu-id="a5b35-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5b35-117">-Confirm</span></span>
<span data-ttu-id="a5b35-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5b35-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b35-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b35-119">-WhatIf</span></span>
<span data-ttu-id="a5b35-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5b35-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b35-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5b35-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b35-122">CommonParameters</span></span>
<span data-ttu-id="a5b35-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5b35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5b35-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b35-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b35-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5b35-125">INPUTS</span></span>

### <span data-ttu-id="a5b35-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="a5b35-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="a5b35-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b35-127">OUTPUTS</span></span>

### <span data-ttu-id="a5b35-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="a5b35-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="a5b35-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5b35-129">NOTES</span></span>

## <span data-ttu-id="a5b35-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b35-130">RELATED LINKS</span></span>
