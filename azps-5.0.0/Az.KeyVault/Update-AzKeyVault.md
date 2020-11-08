---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245276"
---
# <span data-ttu-id="0aa6f-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0aa6f-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="0aa6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0aa6f-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa6f-103">Обновите состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="0aa6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0aa6f-104">SYNTAX</span></span>

### <span data-ttu-id="0aa6f-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0aa6f-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0aa6f-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aa6f-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa6f-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aa6f-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa6f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa6f-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa6f-109">Этот командлет обновляет состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="0aa6f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0aa6f-110">EXAMPLES</span></span>

### <span data-ttu-id="0aa6f-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0aa6f-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="0aa6f-112">Включает защиту от очистки с помощью синтаксиса трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="0aa6f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0aa6f-113">PARAMETERS</span></span>

### <span data-ttu-id="0aa6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa6f-114">-DefaultProfile</span></span>
<span data-ttu-id="0aa6f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa6f-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="0aa6f-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="0aa6f-117">Включите функцию защиты от очистки для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="0aa6f-118">После включения оно не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="0aa6f-119">Для включения требуется мягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="0aa6f-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="0aa6f-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="0aa6f-121">Включение и отключение этого хранилища ключей для авторизации действий с данными с помощью управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="0aa6f-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa6f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aa6f-122">-InputObject</span></span>
<span data-ttu-id="0aa6f-123">Объект хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-123">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0aa6f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa6f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa6f-126">-ResourceId</span></span>
<span data-ttu-id="0aa6f-127">Идентификатор ресурса для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-127">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa6f-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0aa6f-128">-VaultName</span></span>
<span data-ttu-id="0aa6f-129">Имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-129">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa6f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0aa6f-130">-Confirm</span></span>
<span data-ttu-id="0aa6f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa6f-132">-WhatIf</span></span>
<span data-ttu-id="0aa6f-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa6f-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa6f-135">CommonParameters</span></span>
<span data-ttu-id="0aa6f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0aa6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa6f-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0aa6f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa6f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0aa6f-138">INPUTS</span></span>

### <span data-ttu-id="0aa6f-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0aa6f-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0aa6f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa6f-140">System.String</span></span>

## <span data-ttu-id="0aa6f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa6f-141">OUTPUTS</span></span>

### <span data-ttu-id="0aa6f-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0aa6f-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0aa6f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0aa6f-143">NOTES</span></span>

## <span data-ttu-id="0aa6f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aa6f-144">RELATED LINKS</span></span>
