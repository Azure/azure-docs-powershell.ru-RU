---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517661"
---
# <span data-ttu-id="a2486-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2486-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a2486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2486-102">SYNOPSIS</span></span>
<span data-ttu-id="a2486-103">Удаляет политику сетевого доступа JIT.</span><span class="sxs-lookup"><span data-stu-id="a2486-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="a2486-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2486-104">SYNTAX</span></span>

### <span data-ttu-id="a2486-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2486-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2486-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2486-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2486-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2486-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2486-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2486-108">DESCRIPTION</span></span>
<span data-ttu-id="a2486-109">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="a2486-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="a2486-110">После этого действия пользователь не сможет запросить временное сетевое подключение на VMs, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="a2486-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="a2486-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2486-111">EXAMPLES</span></span>

### <span data-ttu-id="a2486-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2486-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="a2486-113">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="a2486-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="a2486-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2486-114">PARAMETERS</span></span>

### <span data-ttu-id="a2486-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2486-115">-DefaultProfile</span></span>
<span data-ttu-id="a2486-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2486-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2486-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2486-117">-InputObject</span></span>
<span data-ttu-id="a2486-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="a2486-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2486-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a2486-119">-Location</span></span>
<span data-ttu-id="a2486-120">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="a2486-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2486-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2486-121">-Name</span></span>
<span data-ttu-id="a2486-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2486-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2486-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2486-123">-PassThru</span></span>
<span data-ttu-id="a2486-124">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="a2486-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a2486-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2486-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2486-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2486-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2486-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2486-127">-ResourceId</span></span>
<span data-ttu-id="a2486-128">ИД ресурса политики сетевого доступа jit.</span><span class="sxs-lookup"><span data-stu-id="a2486-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2486-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2486-129">-Confirm</span></span>
<span data-ttu-id="a2486-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a2486-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2486-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2486-131">-WhatIf</span></span>
<span data-ttu-id="a2486-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2486-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2486-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2486-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2486-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2486-134">CommonParameters</span></span>
<span data-ttu-id="a2486-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2486-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2486-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2486-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2486-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2486-137">INPUTS</span></span>

### <span data-ttu-id="a2486-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a2486-138">System.String</span></span>

### <span data-ttu-id="a2486-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2486-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a2486-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2486-140">OUTPUTS</span></span>

### <span data-ttu-id="a2486-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2486-141">System.Boolean</span></span>

## <span data-ttu-id="a2486-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2486-142">NOTES</span></span>

## <span data-ttu-id="a2486-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2486-143">RELATED LINKS</span></span>
