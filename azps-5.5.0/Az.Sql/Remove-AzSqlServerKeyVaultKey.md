---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231721"
---
# <span data-ttu-id="f257b-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f257b-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f257b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f257b-102">SYNOPSIS</span></span>
<span data-ttu-id="f257b-103">Удаляет ключ из хранилища ключей с SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="f257b-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="f257b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f257b-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f257b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f257b-105">DESCRIPTION</span></span>
<span data-ttu-id="f257b-106">Этот Remove-AzSqlServerKeyVaultKey удаляет ключ сейфа с указанного SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="f257b-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="f257b-107">Обратите внимание SQL что разрешения сервера для хранилища ключа не меняются.</span><span class="sxs-lookup"><span data-stu-id="f257b-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="f257b-108">Чтобы изменить разрешения, используйте Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="f257b-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="f257b-109">Обратите внимание, что этот cmdlet не изменяет хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f257b-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="f257b-110">Чтобы удалить ключ из key Vault, используйте Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="f257b-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="f257b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f257b-111">EXAMPLES</span></span>

### <span data-ttu-id="f257b-112">Пример 1. Удаление ключа сейфа</span><span class="sxs-lookup"><span data-stu-id="f257b-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f257b-113">Эта команда удаляет ключ сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="f257b-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="f257b-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 11223344556678899001122334455677889900 CreationDate: 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="f257b-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="f257b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f257b-115">PARAMETERS</span></span>

### <span data-ttu-id="f257b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f257b-116">-AsJob</span></span>
<span data-ttu-id="f257b-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f257b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f257b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f257b-118">-DefaultProfile</span></span>
<span data-ttu-id="f257b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f257b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f257b-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f257b-120">-KeyId</span></span>
<span data-ttu-id="f257b-121">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="f257b-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="f257b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f257b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f257b-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f257b-123">The name of the resource group</span></span>

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

### <span data-ttu-id="f257b-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f257b-124">-ServerName</span></span>
<span data-ttu-id="f257b-125">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="f257b-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f257b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f257b-126">-Confirm</span></span>
<span data-ttu-id="f257b-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f257b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f257b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f257b-128">-WhatIf</span></span>
<span data-ttu-id="f257b-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f257b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f257b-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f257b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f257b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f257b-131">CommonParameters</span></span>
<span data-ttu-id="f257b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f257b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f257b-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f257b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f257b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f257b-134">INPUTS</span></span>

### <span data-ttu-id="f257b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f257b-135">System.String</span></span>

## <span data-ttu-id="f257b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f257b-136">OUTPUTS</span></span>

### <span data-ttu-id="f257b-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f257b-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f257b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f257b-138">NOTES</span></span>

## <span data-ttu-id="f257b-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f257b-139">RELATED LINKS</span></span>

[<span data-ttu-id="f257b-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f257b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
