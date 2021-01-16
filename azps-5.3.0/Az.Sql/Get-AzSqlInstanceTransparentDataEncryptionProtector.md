---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506638"
---
# <span data-ttu-id="8c50d-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8c50d-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="8c50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c50d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c50d-103">Получает прозрачный защита шифрования данных (TDE) для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8c50d-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="8c50d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c50d-104">SYNTAX</span></span>

### <span data-ttu-id="8c50d-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c50d-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c50d-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c50d-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c50d-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c50d-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c50d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c50d-108">DESCRIPTION</span></span>
<span data-ttu-id="8c50d-109">Этот Get-AzSqlInstanceTransparentDataEncryptionProtector получает защиту TDE для указанного SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8c50d-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="8c50d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c50d-110">EXAMPLES</span></span>

### <span data-ttu-id="8c50d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c50d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c50d-112">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c50d-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c50d-113">Пример 2. Использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="8c50d-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c50d-114">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c50d-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c50d-115">Пример 3. Использование ИД ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="8c50d-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c50d-116">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c50d-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c50d-117">Пример 4. Использование piping</span><span class="sxs-lookup"><span data-stu-id="8c50d-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c50d-118">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c50d-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8c50d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c50d-119">PARAMETERS</span></span>

### <span data-ttu-id="8c50d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c50d-120">-DefaultProfile</span></span>
<span data-ttu-id="8c50d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c50d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c50d-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="8c50d-122">-Instance</span></span>
<span data-ttu-id="8c50d-123">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="8c50d-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c50d-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8c50d-124">-InstanceName</span></span>
<span data-ttu-id="8c50d-125">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="8c50d-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c50d-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="8c50d-126">-InstanceResourceId</span></span>
<span data-ttu-id="8c50d-127">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="8c50d-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c50d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c50d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c50d-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8c50d-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c50d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c50d-130">-Confirm</span></span>
<span data-ttu-id="8c50d-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8c50d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c50d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c50d-132">-WhatIf</span></span>
<span data-ttu-id="8c50d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c50d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c50d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c50d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c50d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c50d-135">CommonParameters</span></span>
<span data-ttu-id="8c50d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c50d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c50d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c50d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c50d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c50d-138">INPUTS</span></span>

### <span data-ttu-id="8c50d-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8c50d-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="8c50d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c50d-140">System.String</span></span>

## <span data-ttu-id="8c50d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c50d-141">OUTPUTS</span></span>

### <span data-ttu-id="8c50d-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="8c50d-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="8c50d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c50d-143">NOTES</span></span>

## <span data-ttu-id="8c50d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c50d-144">RELATED LINKS</span></span>
