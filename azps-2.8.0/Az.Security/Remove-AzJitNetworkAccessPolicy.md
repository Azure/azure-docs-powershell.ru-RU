---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b0414b6fbbd4cdb0211b7dee1f85e172c1329c3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905417"
---
# <span data-ttu-id="89ad3-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89ad3-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="89ad3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="89ad3-103">Удаление политики доступа по JIT-сети.</span><span class="sxs-lookup"><span data-stu-id="89ad3-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="89ad3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ad3-104">SYNTAX</span></span>

### <span data-ttu-id="89ad3-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89ad3-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ad3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ad3-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ad3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="89ad3-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ad3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ad3-108">DESCRIPTION</span></span>
<span data-ttu-id="89ad3-109">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="89ad3-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="89ad3-110">После этого пользователь не сможет запросить временное сетевое подключение на виртуальных машинах, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="89ad3-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="89ad3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ad3-111">EXAMPLES</span></span>

### <span data-ttu-id="89ad3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89ad3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="89ad3-113">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="89ad3-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="89ad3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ad3-114">PARAMETERS</span></span>

### <span data-ttu-id="89ad3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ad3-115">-DefaultProfile</span></span>
<span data-ttu-id="89ad3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89ad3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ad3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ad3-117">-InputObject</span></span>
<span data-ttu-id="89ad3-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="89ad3-118">Input Object.</span></span>

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

### <span data-ttu-id="89ad3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="89ad3-119">-Location</span></span>
<span data-ttu-id="89ad3-120">Поиска.</span><span class="sxs-lookup"><span data-stu-id="89ad3-120">Location.</span></span>

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

### <span data-ttu-id="89ad3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89ad3-121">-Name</span></span>
<span data-ttu-id="89ad3-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="89ad3-122">Resource name.</span></span>

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

### <span data-ttu-id="89ad3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89ad3-123">-PassThru</span></span>
<span data-ttu-id="89ad3-124">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="89ad3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="89ad3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ad3-125">-ResourceGroupName</span></span>
<span data-ttu-id="89ad3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89ad3-126">Resource group name.</span></span>

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

### <span data-ttu-id="89ad3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ad3-127">-ResourceId</span></span>
<span data-ttu-id="89ad3-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="89ad3-128">Resource ID.</span></span>

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

### <span data-ttu-id="89ad3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89ad3-129">-Confirm</span></span>
<span data-ttu-id="89ad3-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89ad3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ad3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ad3-131">-WhatIf</span></span>
<span data-ttu-id="89ad3-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89ad3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89ad3-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89ad3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ad3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ad3-134">CommonParameters</span></span>
<span data-ttu-id="89ad3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ad3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ad3-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ad3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ad3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ad3-137">INPUTS</span></span>

### <span data-ttu-id="89ad3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89ad3-138">System.String</span></span>

### <span data-ttu-id="89ad3-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89ad3-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="89ad3-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ad3-140">OUTPUTS</span></span>

### <span data-ttu-id="89ad3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ad3-141">System.Boolean</span></span>

## <span data-ttu-id="89ad3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ad3-142">NOTES</span></span>

## <span data-ttu-id="89ad3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ad3-143">RELATED LINKS</span></span>
