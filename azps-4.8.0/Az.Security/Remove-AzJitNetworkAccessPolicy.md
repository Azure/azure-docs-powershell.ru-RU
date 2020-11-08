---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243974"
---
# <span data-ttu-id="8e311-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e311-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8e311-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e311-102">SYNOPSIS</span></span>
<span data-ttu-id="8e311-103">Удаление политики доступа по JIT-сети.</span><span class="sxs-lookup"><span data-stu-id="8e311-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="8e311-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e311-104">SYNTAX</span></span>

### <span data-ttu-id="8e311-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e311-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e311-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e311-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e311-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e311-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e311-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e311-108">DESCRIPTION</span></span>
<span data-ttu-id="8e311-109">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="8e311-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="8e311-110">После этого пользователь не сможет запросить временное сетевое подключение на виртуальных машинах, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="8e311-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="8e311-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e311-111">EXAMPLES</span></span>

### <span data-ttu-id="8e311-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e311-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="8e311-113">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="8e311-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="8e311-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e311-114">PARAMETERS</span></span>

### <span data-ttu-id="8e311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e311-115">-DefaultProfile</span></span>
<span data-ttu-id="8e311-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e311-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e311-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e311-117">-InputObject</span></span>
<span data-ttu-id="8e311-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="8e311-118">Input Object.</span></span>

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

### <span data-ttu-id="8e311-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8e311-119">-Location</span></span>
<span data-ttu-id="8e311-120">Поиска.</span><span class="sxs-lookup"><span data-stu-id="8e311-120">Location.</span></span>

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

### <span data-ttu-id="8e311-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e311-121">-Name</span></span>
<span data-ttu-id="8e311-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e311-122">Resource name.</span></span>

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

### <span data-ttu-id="8e311-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e311-123">-PassThru</span></span>
<span data-ttu-id="8e311-124">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8e311-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8e311-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e311-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e311-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e311-126">Resource group name.</span></span>

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

### <span data-ttu-id="8e311-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e311-127">-ResourceId</span></span>
<span data-ttu-id="8e311-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e311-128">Resource ID.</span></span>

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

### <span data-ttu-id="8e311-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e311-129">-Confirm</span></span>
<span data-ttu-id="8e311-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e311-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e311-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e311-131">-WhatIf</span></span>
<span data-ttu-id="8e311-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e311-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e311-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e311-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e311-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e311-134">CommonParameters</span></span>
<span data-ttu-id="8e311-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e311-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e311-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e311-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e311-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e311-137">INPUTS</span></span>

### <span data-ttu-id="8e311-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e311-138">System.String</span></span>

### <span data-ttu-id="8e311-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e311-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8e311-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e311-140">OUTPUTS</span></span>

### <span data-ttu-id="8e311-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e311-141">System.Boolean</span></span>

## <span data-ttu-id="8e311-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e311-142">NOTES</span></span>

## <span data-ttu-id="8e311-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e311-143">RELATED LINKS</span></span>
