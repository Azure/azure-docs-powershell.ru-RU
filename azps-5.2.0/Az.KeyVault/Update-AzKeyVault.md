---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394436"
---
# <span data-ttu-id="70343-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="70343-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="70343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70343-102">SYNOPSIS</span></span>
<span data-ttu-id="70343-103">Обновление состояния хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="70343-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="70343-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70343-104">SYNTAX</span></span>

### <span data-ttu-id="70343-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70343-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70343-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70343-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70343-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70343-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70343-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70343-108">DESCRIPTION</span></span>
<span data-ttu-id="70343-109">Этот cmdlet обновляет состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="70343-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="70343-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70343-110">EXAMPLES</span></span>

### <span data-ttu-id="70343-111">Пример 1. Защита очистки</span><span class="sxs-lookup"><span data-stu-id="70343-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="70343-112">Обеспечивает очистку защиты с использованием синтаксиса piping.</span><span class="sxs-lookup"><span data-stu-id="70343-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="70343-113">Пример 2. Включить авторизацию с помощью RBAC</span><span class="sxs-lookup"><span data-stu-id="70343-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="70343-114">Включает авторизацию СРAC с использованием синтаксиса piping.</span><span class="sxs-lookup"><span data-stu-id="70343-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="70343-115">Пример 3. Настройка тегов</span><span class="sxs-lookup"><span data-stu-id="70343-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="70343-116">Задает теги ключного сейфа с $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="70343-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="70343-117">Пример 4. Очистка тегов</span><span class="sxs-lookup"><span data-stu-id="70343-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="70343-118">Удаляет все теги ключного сейфа с $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="70343-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="70343-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70343-119">PARAMETERS</span></span>

### <span data-ttu-id="70343-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70343-120">-DefaultProfile</span></span>
<span data-ttu-id="70343-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70343-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70343-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="70343-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="70343-123">В этой области можно включить функцию защиты очистки для этого сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="70343-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="70343-124">После включения его невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="70343-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="70343-125">Для этого требуется обратимый удаление.</span><span class="sxs-lookup"><span data-stu-id="70343-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="70343-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="70343-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="70343-127">Включив или отключив этот ключ, можно разрешить действия с данными с помощью управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="70343-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="70343-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70343-128">-InputObject</span></span>
<span data-ttu-id="70343-129">Объект key vault.</span><span class="sxs-lookup"><span data-stu-id="70343-129">Key vault object.</span></span>

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

### <span data-ttu-id="70343-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70343-130">-ResourceGroupName</span></span>
<span data-ttu-id="70343-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70343-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="70343-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70343-132">-ResourceId</span></span>
<span data-ttu-id="70343-133">ИД ресурса хранилища ключа.</span><span class="sxs-lookup"><span data-stu-id="70343-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="70343-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="70343-134">-Tag</span></span>
<span data-ttu-id="70343-135">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="70343-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70343-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70343-136">-VaultName</span></span>
<span data-ttu-id="70343-137">Имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="70343-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="70343-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70343-138">-Confirm</span></span>
<span data-ttu-id="70343-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="70343-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70343-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70343-140">-WhatIf</span></span>
<span data-ttu-id="70343-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70343-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70343-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="70343-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70343-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70343-143">CommonParameters</span></span>
<span data-ttu-id="70343-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70343-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70343-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70343-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70343-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70343-146">INPUTS</span></span>

### <span data-ttu-id="70343-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="70343-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="70343-148">System.String</span><span class="sxs-lookup"><span data-stu-id="70343-148">System.String</span></span>

## <span data-ttu-id="70343-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70343-149">OUTPUTS</span></span>

### <span data-ttu-id="70343-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="70343-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="70343-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70343-151">NOTES</span></span>

## <span data-ttu-id="70343-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70343-152">RELATED LINKS</span></span>
