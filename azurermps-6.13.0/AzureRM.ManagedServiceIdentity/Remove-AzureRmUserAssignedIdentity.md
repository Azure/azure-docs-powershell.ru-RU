---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734359"
---
# <span data-ttu-id="9598f-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9598f-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="9598f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9598f-102">SYNOPSIS</span></span>
<span data-ttu-id="9598f-103">Удаляет пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="9598f-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9598f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9598f-104">SYNTAX</span></span>

### <span data-ttu-id="9598f-105">ResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9598f-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9598f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9598f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9598f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9598f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9598f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9598f-108">DESCRIPTION</span></span>
<span data-ttu-id="9598f-109">Средство **Remove-AzureRmUserAssignedIdentity** Удаляет указанного пользователя, которому назначено удостоверение.</span><span class="sxs-lookup"><span data-stu-id="9598f-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="9598f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9598f-110">EXAMPLES</span></span>

### <span data-ttu-id="9598f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9598f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="9598f-112">В этом примере командлет удаляет удостоверение **id1** в разделе "Группа ресурсов" **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="9598f-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="9598f-113">Задан</span><span class="sxs-lookup"><span data-stu-id="9598f-113">True</span></span>

## <span data-ttu-id="9598f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9598f-114">PARAMETERS</span></span>

### <span data-ttu-id="9598f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9598f-115">-AsJob</span></span>
<span data-ttu-id="9598f-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9598f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9598f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9598f-117">-DefaultProfile</span></span>
<span data-ttu-id="9598f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9598f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9598f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9598f-119">-Force</span></span>
<span data-ttu-id="9598f-120">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="9598f-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="9598f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9598f-121">-InputObject</span></span>
<span data-ttu-id="9598f-122">Объект Identity.</span><span class="sxs-lookup"><span data-stu-id="9598f-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9598f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9598f-123">-Name</span></span>
<span data-ttu-id="9598f-124">Имя удостоверения.</span><span class="sxs-lookup"><span data-stu-id="9598f-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9598f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9598f-125">-ResourceGroupName</span></span>
<span data-ttu-id="9598f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9598f-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9598f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9598f-127">-ResourceId</span></span>
<span data-ttu-id="9598f-128">Идентификатор ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="9598f-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9598f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9598f-129">-Confirm</span></span>
<span data-ttu-id="9598f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9598f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9598f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9598f-131">-WhatIf</span></span>
<span data-ttu-id="9598f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9598f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9598f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9598f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9598f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9598f-134">CommonParameters</span></span>
<span data-ttu-id="9598f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9598f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9598f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9598f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9598f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9598f-137">INPUTS</span></span>

### <span data-ttu-id="9598f-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9598f-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="9598f-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9598f-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9598f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9598f-140">System.String</span></span>

## <span data-ttu-id="9598f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9598f-141">OUTPUTS</span></span>

### <span data-ttu-id="9598f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9598f-142">System.Boolean</span></span>

## <span data-ttu-id="9598f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9598f-143">NOTES</span></span>

## <span data-ttu-id="9598f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9598f-144">RELATED LINKS</span></span>
