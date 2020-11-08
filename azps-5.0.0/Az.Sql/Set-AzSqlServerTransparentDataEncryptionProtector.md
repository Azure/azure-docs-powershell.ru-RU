---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249782"
---
# <span data-ttu-id="81480-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="81480-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="81480-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81480-102">SYNOPSIS</span></span>
<span data-ttu-id="81480-103">Установка предохранителя прозрачного шифрования данных (TDE) для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81480-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="81480-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81480-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81480-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81480-105">DESCRIPTION</span></span>
<span data-ttu-id="81480-106">Командлет Set-AzSqlServerTransparentDataEncryptionProtector задает предохранитель TDE для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81480-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="81480-107">Изменение типа предохранителя TDE приводит к повернутию предохранителя.</span><span class="sxs-lookup"><span data-stu-id="81480-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="81480-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81480-108">EXAMPLES</span></span>

### <span data-ttu-id="81480-109">Пример 1: Настройка типа предохранителя прозрачного шифрования данных (TDE) на ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="81480-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="81480-110">Эта команда обновляет Тип предохранителя сервера TDE для управления службами.</span><span class="sxs-lookup"><span data-stu-id="81480-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="81480-111">ResourceGroupName ИмяСервера Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="81480-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="81480-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="81480-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="81480-113">Пример 2: Установка прозрачного типа предохранителя для шифрования данных Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="81480-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="81480-114">Эта команда обновляет сервер для использования ключа хранилища ключей сервера с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="81480-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="81480-115">ResourceGroupName ИмяСервера Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="81480-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="81480-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="81480-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="81480-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81480-117">PARAMETERS</span></span>

### <span data-ttu-id="81480-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81480-118">-AsJob</span></span>
<span data-ttu-id="81480-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="81480-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81480-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81480-120">-DefaultProfile</span></span>
<span data-ttu-id="81480-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81480-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81480-122">-Force</span><span class="sxs-lookup"><span data-stu-id="81480-122">-Force</span></span>
<span data-ttu-id="81480-123">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="81480-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="81480-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="81480-124">-KeyId</span></span>
<span data-ttu-id="81480-125">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="81480-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81480-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81480-126">-ResourceGroupName</span></span>
<span data-ttu-id="81480-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81480-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81480-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="81480-128">-ServerName</span></span>
<span data-ttu-id="81480-129">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81480-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81480-130">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="81480-130">-Type</span></span>
<span data-ttu-id="81480-131">Тип предохранителя базы данных SQL Azure TDE.</span><span class="sxs-lookup"><span data-stu-id="81480-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81480-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81480-132">-Confirm</span></span>
<span data-ttu-id="81480-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81480-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81480-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81480-134">-WhatIf</span></span>
<span data-ttu-id="81480-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81480-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81480-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81480-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81480-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81480-137">CommonParameters</span></span>
<span data-ttu-id="81480-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81480-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81480-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81480-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81480-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81480-140">INPUTS</span></span>

### <span data-ttu-id="81480-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="81480-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="81480-142">System. String</span><span class="sxs-lookup"><span data-stu-id="81480-142">System.String</span></span>

## <span data-ttu-id="81480-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81480-143">OUTPUTS</span></span>

### <span data-ttu-id="81480-144">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="81480-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="81480-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="81480-145">NOTES</span></span>

## <span data-ttu-id="81480-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81480-146">RELATED LINKS</span></span>

[<span data-ttu-id="81480-147">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="81480-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
