---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246520"
---
# <span data-ttu-id="181a0-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="181a0-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="181a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="181a0-102">SYNOPSIS</span></span>
<span data-ttu-id="181a0-103">Удаление ключа хранилища ключей из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="181a0-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="181a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="181a0-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="181a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="181a0-105">DESCRIPTION</span></span>
<span data-ttu-id="181a0-106">Командлет Remove-AzSqlServerKeyVaultKey удаляет ключ хранилища ключей из указанного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="181a0-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="181a0-107">Обратите внимание, что разрешения SQL Server для хранилища ключа не изменяются.</span><span class="sxs-lookup"><span data-stu-id="181a0-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="181a0-108">Чтобы изменить разрешения, используйте Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="181a0-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="181a0-109">Обратите внимание, что этот командлет не вносит изменения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="181a0-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="181a0-110">Чтобы удалить раздел из хранилища ключей, используйте Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="181a0-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="181a0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="181a0-111">EXAMPLES</span></span>

### <span data-ttu-id="181a0-112">Пример 1: Удаление ключа хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="181a0-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="181a0-113">Эта команда удаляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="181a0-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="181a0-114">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="181a0-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="181a0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="181a0-115">PARAMETERS</span></span>

### <span data-ttu-id="181a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="181a0-116">-AsJob</span></span>
<span data-ttu-id="181a0-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="181a0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="181a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181a0-118">-DefaultProfile</span></span>
<span data-ttu-id="181a0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="181a0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="181a0-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="181a0-120">-KeyId</span></span>
<span data-ttu-id="181a0-121">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="181a0-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="181a0-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="181a0-123">The name of the resource group</span></span>

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

### <span data-ttu-id="181a0-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="181a0-124">-ServerName</span></span>
<span data-ttu-id="181a0-125">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="181a0-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="181a0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="181a0-126">-Confirm</span></span>
<span data-ttu-id="181a0-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="181a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="181a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="181a0-128">-WhatIf</span></span>
<span data-ttu-id="181a0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="181a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="181a0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="181a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="181a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181a0-131">CommonParameters</span></span>
<span data-ttu-id="181a0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="181a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181a0-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="181a0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181a0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="181a0-134">INPUTS</span></span>

### <span data-ttu-id="181a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="181a0-135">System.String</span></span>

## <span data-ttu-id="181a0-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="181a0-136">OUTPUTS</span></span>

### <span data-ttu-id="181a0-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="181a0-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="181a0-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="181a0-138">NOTES</span></span>

## <span data-ttu-id="181a0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="181a0-139">RELATED LINKS</span></span>

[<span data-ttu-id="181a0-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="181a0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
