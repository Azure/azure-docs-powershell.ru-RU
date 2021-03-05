---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 7220304c4dbc234a3513d2dfc35e6d71180159e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003091"
---
# <span data-ttu-id="54d28-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54d28-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="54d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d28-102">SYNOPSIS</span></span>
<span data-ttu-id="54d28-103">Удаляет политику сетевого доступа JIT.</span><span class="sxs-lookup"><span data-stu-id="54d28-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="54d28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54d28-104">SYNTAX</span></span>

### <span data-ttu-id="54d28-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54d28-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d28-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54d28-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d28-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="54d28-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d28-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54d28-108">DESCRIPTION</span></span>
<span data-ttu-id="54d28-109">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="54d28-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="54d28-110">После этого действия пользователь не сможет запросить временное сетевое подключение на VMs, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="54d28-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="54d28-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54d28-111">EXAMPLES</span></span>

### <span data-ttu-id="54d28-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54d28-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="54d28-113">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="54d28-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="54d28-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d28-114">PARAMETERS</span></span>

### <span data-ttu-id="54d28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d28-115">-DefaultProfile</span></span>
<span data-ttu-id="54d28-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54d28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54d28-117">-InputObject</span></span>
<span data-ttu-id="54d28-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="54d28-118">Input Object.</span></span>

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

### <span data-ttu-id="54d28-119">-Location</span><span class="sxs-lookup"><span data-stu-id="54d28-119">-Location</span></span>
<span data-ttu-id="54d28-120">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="54d28-120">Location.</span></span>

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

### <span data-ttu-id="54d28-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54d28-121">-Name</span></span>
<span data-ttu-id="54d28-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="54d28-122">Resource name.</span></span>

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

### <span data-ttu-id="54d28-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d28-123">-PassThru</span></span>
<span data-ttu-id="54d28-124">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="54d28-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="54d28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d28-125">-ResourceGroupName</span></span>
<span data-ttu-id="54d28-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54d28-126">Resource group name.</span></span>

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

### <span data-ttu-id="54d28-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54d28-127">-ResourceId</span></span>
<span data-ttu-id="54d28-128">ИД ресурса политики сетевого доступа jit.</span><span class="sxs-lookup"><span data-stu-id="54d28-128">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="54d28-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54d28-129">-Confirm</span></span>
<span data-ttu-id="54d28-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d28-131">-WhatIf</span></span>
<span data-ttu-id="54d28-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d28-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d28-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54d28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d28-134">CommonParameters</span></span>
<span data-ttu-id="54d28-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d28-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54d28-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d28-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54d28-137">INPUTS</span></span>

### <span data-ttu-id="54d28-138">System.String</span><span class="sxs-lookup"><span data-stu-id="54d28-138">System.String</span></span>

### <span data-ttu-id="54d28-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54d28-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="54d28-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54d28-140">OUTPUTS</span></span>

### <span data-ttu-id="54d28-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54d28-141">System.Boolean</span></span>

## <span data-ttu-id="54d28-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54d28-142">NOTES</span></span>

## <span data-ttu-id="54d28-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54d28-143">RELATED LINKS</span></span>
