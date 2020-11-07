---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735027"
---
# <span data-ttu-id="a4fc8-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a4fc8-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="a4fc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fc8-103">Установка предохранителя прозрачного шифрования данных (TDE) для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4fc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4fc8-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="a4fc8-106">Командлет Set-AzureRmSqlServerTransparentDataEncryptionProtector задает предохранитель TDE для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="a4fc8-107">Изменение типа предохранителя TDE приводит к повернутию предохранителя.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="a4fc8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4fc8-108">EXAMPLES</span></span>

### <span data-ttu-id="a4fc8-109">--------------------------Пример 1: установите для типа предохранителя прозрачное шифрование данных (TDE) значение ServiceManaged--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4fc8-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="a4fc8-110">Эта команда обновляет Тип предохранителя сервера TDE для управления службами.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="a4fc8-111">ResourceGroupName ИмяСервера Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="a4fc8-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="a4fc8-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="a4fc8-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="a4fc8-113">--------------------------Пример 2: задайте для типа предохранителя прозрачность шифрования данных Azure Key Vault--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4fc8-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="a4fc8-114">Эта команда обновляет сервер для использования ключа хранилища ключей сервера с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="a4fc8-115">ResourceGroupName ИмяСервера Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="a4fc8-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="a4fc8-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="a4fc8-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="a4fc8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4fc8-117">PARAMETERS</span></span>

### <span data-ttu-id="a4fc8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a4fc8-118">-Force</span></span>
<span data-ttu-id="a4fc8-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="a4fc8-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a4fc8-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a4fc8-120">-KeyId</span></span>
<span data-ttu-id="a4fc8-121">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="a4fc8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4fc8-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4fc8-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-123">The name of the resource group</span></span>

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

### <span data-ttu-id="a4fc8-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a4fc8-124">-ServerName</span></span>
<span data-ttu-id="a4fc8-125">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a4fc8-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a4fc8-126">-Type</span></span>
<span data-ttu-id="a4fc8-127">Тип предохранителя базы данных SQL Azure TDE.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="a4fc8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4fc8-128">-Confirm</span></span>
<span data-ttu-id="a4fc8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fc8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fc8-130">-WhatIf</span></span>
<span data-ttu-id="a4fc8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fc8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fc8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fc8-133">-DefaultProfile</span></span>
<span data-ttu-id="a4fc8-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4fc8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fc8-135">CommonParameters</span></span>
<span data-ttu-id="a4fc8-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fc8-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fc8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fc8-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4fc8-138">INPUTS</span></span>

### <span data-ttu-id="a4fc8-139">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="a4fc8-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="a4fc8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fc8-140">System.String</span></span>

## <span data-ttu-id="a4fc8-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc8-141">OUTPUTS</span></span>

### <span data-ttu-id="a4fc8-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="a4fc8-142">System.Object</span></span>

## <span data-ttu-id="a4fc8-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4fc8-143">NOTES</span></span>

## <span data-ttu-id="a4fc8-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4fc8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a4fc8-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a4fc8-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
