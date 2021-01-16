---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325223"
---
# <span data-ttu-id="c2b27-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c2b27-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c2b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b27-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b27-103">Получает прозрачный защита шифрования данных (TDE) для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c2b27-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c2b27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2b27-104">SYNTAX</span></span>

### <span data-ttu-id="c2b27-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2b27-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b27-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b27-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b27-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b27-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b27-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2b27-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b27-109">Этот Get-AzSqlInstanceTransparentDataEncryptionProtector получает защиту TDE для указанного SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c2b27-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="c2b27-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2b27-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b27-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2b27-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2b27-112">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2b27-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2b27-113">Пример 2. Использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2b27-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2b27-114">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2b27-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2b27-115">Пример 3. Использование ИД ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2b27-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2b27-116">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2b27-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2b27-117">Пример 4. Использование piping</span><span class="sxs-lookup"><span data-stu-id="c2b27-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2b27-118">Эта команда получает защиту TDE для управляемого экземпляра ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2b27-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c2b27-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2b27-119">PARAMETERS</span></span>

### <span data-ttu-id="c2b27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b27-120">-DefaultProfile</span></span>
<span data-ttu-id="c2b27-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b27-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b27-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="c2b27-122">-Instance</span></span>
<span data-ttu-id="c2b27-123">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2b27-123">The instance input object</span></span>

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

### <span data-ttu-id="c2b27-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2b27-124">-InstanceName</span></span>
<span data-ttu-id="c2b27-125">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2b27-125">The instance name</span></span>

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

### <span data-ttu-id="c2b27-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b27-126">-InstanceResourceId</span></span>
<span data-ttu-id="c2b27-127">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2b27-127">The instance resource id</span></span>

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

### <span data-ttu-id="c2b27-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b27-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2b27-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2b27-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="c2b27-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2b27-130">-Confirm</span></span>
<span data-ttu-id="c2b27-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b27-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b27-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b27-132">-WhatIf</span></span>
<span data-ttu-id="c2b27-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b27-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b27-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2b27-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b27-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b27-135">CommonParameters</span></span>
<span data-ttu-id="c2b27-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b27-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b27-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2b27-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b27-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2b27-138">INPUTS</span></span>

### <span data-ttu-id="c2b27-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c2b27-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c2b27-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c2b27-140">System.String</span></span>

## <span data-ttu-id="c2b27-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2b27-141">OUTPUTS</span></span>

### <span data-ttu-id="c2b27-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="c2b27-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c2b27-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2b27-143">NOTES</span></span>

## <span data-ttu-id="c2b27-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2b27-144">RELATED LINKS</span></span>