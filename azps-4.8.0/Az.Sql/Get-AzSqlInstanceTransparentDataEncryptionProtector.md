---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243921"
---
# <span data-ttu-id="cef2b-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cef2b-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="cef2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cef2b-102">SYNOPSIS</span></span>
<span data-ttu-id="cef2b-103">Получает предохранитель прозрачного шифрования данных (TDE) для экземпляра, управляемого SQL.</span><span class="sxs-lookup"><span data-stu-id="cef2b-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="cef2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cef2b-104">SYNTAX</span></span>

### <span data-ttu-id="cef2b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef2b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef2b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef2b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef2b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef2b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef2b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef2b-108">DESCRIPTION</span></span>
<span data-ttu-id="cef2b-109">Командлет Get-AzSqlInstanceTransparentDataEncryptionProtector получает предохранитель TDE для указанного управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cef2b-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="cef2b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cef2b-110">EXAMPLES</span></span>

### <span data-ttu-id="cef2b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cef2b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="cef2b-112">Эта команда получает предохранитель TDE для управляемого экземпляра с именем ContosoManagedInstanceName в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cef2b-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="cef2b-113">Пример 2: использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="cef2b-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="cef2b-114">Эта команда получает предохранитель TDE для управляемого экземпляра с именем ContosoManagedInstanceName в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cef2b-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="cef2b-115">Пример 3: использование идентификатора ресурса управляемых экземпляров</span><span class="sxs-lookup"><span data-stu-id="cef2b-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="cef2b-116">Эта команда получает предохранитель TDE для управляемого экземпляра с именем ContosoManagedInstanceName в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cef2b-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="cef2b-117">Пример 4: использование трубопроводов</span><span class="sxs-lookup"><span data-stu-id="cef2b-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="cef2b-118">Эта команда получает предохранитель TDE для управляемого экземпляра с именем ContosoManagedInstanceName в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cef2b-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="cef2b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cef2b-119">PARAMETERS</span></span>

### <span data-ttu-id="cef2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef2b-120">-DefaultProfile</span></span>
<span data-ttu-id="cef2b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef2b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef2b-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="cef2b-122">-Instance</span></span>
<span data-ttu-id="cef2b-123">Входной объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="cef2b-123">The instance input object</span></span>

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

### <span data-ttu-id="cef2b-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cef2b-124">-InstanceName</span></span>
<span data-ttu-id="cef2b-125">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cef2b-125">The instance name</span></span>

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

### <span data-ttu-id="cef2b-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cef2b-126">-InstanceResourceId</span></span>
<span data-ttu-id="cef2b-127">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="cef2b-127">The instance resource id</span></span>

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

### <span data-ttu-id="cef2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="cef2b-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cef2b-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="cef2b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef2b-130">-Confirm</span></span>
<span data-ttu-id="cef2b-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cef2b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef2b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef2b-132">-WhatIf</span></span>
<span data-ttu-id="cef2b-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cef2b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef2b-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cef2b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef2b-135">CommonParameters</span></span>
<span data-ttu-id="cef2b-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cef2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef2b-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cef2b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef2b-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cef2b-138">INPUTS</span></span>

### <span data-ttu-id="cef2b-139">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cef2b-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="cef2b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cef2b-140">System.String</span></span>

## <span data-ttu-id="cef2b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef2b-141">OUTPUTS</span></span>

### <span data-ttu-id="cef2b-142">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="cef2b-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="cef2b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cef2b-143">NOTES</span></span>

## <span data-ttu-id="cef2b-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef2b-144">RELATED LINKS</span></span>
