---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395980"
---
# <span data-ttu-id="73cc2-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73cc2-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="73cc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="73cc2-103">Удаляет политику сетевого доступа JIT.</span><span class="sxs-lookup"><span data-stu-id="73cc2-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="73cc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73cc2-104">SYNTAX</span></span>

### <span data-ttu-id="73cc2-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73cc2-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cc2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="73cc2-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cc2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="73cc2-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73cc2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="73cc2-109">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="73cc2-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="73cc2-110">После этого действия пользователь не сможет запросить временное сетевое подключение на VMs, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="73cc2-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="73cc2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73cc2-111">EXAMPLES</span></span>

### <span data-ttu-id="73cc2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73cc2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="73cc2-113">Удаляет политику сетевого доступа "Только вовремя".</span><span class="sxs-lookup"><span data-stu-id="73cc2-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="73cc2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73cc2-114">PARAMETERS</span></span>

### <span data-ttu-id="73cc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cc2-115">-DefaultProfile</span></span>
<span data-ttu-id="73cc2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73cc2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73cc2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73cc2-117">-InputObject</span></span>
<span data-ttu-id="73cc2-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="73cc2-118">Input Object.</span></span>

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

### <span data-ttu-id="73cc2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="73cc2-119">-Location</span></span>
<span data-ttu-id="73cc2-120">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="73cc2-120">Location.</span></span>

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

### <span data-ttu-id="73cc2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73cc2-121">-Name</span></span>
<span data-ttu-id="73cc2-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="73cc2-122">Resource name.</span></span>

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

### <span data-ttu-id="73cc2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73cc2-123">-PassThru</span></span>
<span data-ttu-id="73cc2-124">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="73cc2-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="73cc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73cc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="73cc2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73cc2-126">Resource group name.</span></span>

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

### <span data-ttu-id="73cc2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73cc2-127">-ResourceId</span></span>
<span data-ttu-id="73cc2-128">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="73cc2-128">Resource ID.</span></span>

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

### <span data-ttu-id="73cc2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73cc2-129">-Confirm</span></span>
<span data-ttu-id="73cc2-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73cc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cc2-131">-WhatIf</span></span>
<span data-ttu-id="73cc2-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cc2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73cc2-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73cc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73cc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cc2-134">CommonParameters</span></span>
<span data-ttu-id="73cc2-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cc2-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73cc2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cc2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73cc2-137">INPUTS</span></span>

### <span data-ttu-id="73cc2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="73cc2-138">System.String</span></span>

### <span data-ttu-id="73cc2-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73cc2-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="73cc2-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73cc2-140">OUTPUTS</span></span>

### <span data-ttu-id="73cc2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73cc2-141">System.Boolean</span></span>

## <span data-ttu-id="73cc2-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73cc2-142">NOTES</span></span>

## <span data-ttu-id="73cc2-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73cc2-143">RELATED LINKS</span></span>
