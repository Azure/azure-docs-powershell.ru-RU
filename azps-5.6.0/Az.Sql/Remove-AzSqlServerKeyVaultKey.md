---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967347"
---
# <span data-ttu-id="17c96-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17c96-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="17c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c96-102">SYNOPSIS</span></span>
<span data-ttu-id="17c96-103">Удаляет ключ сейфа с SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="17c96-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="17c96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17c96-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17c96-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17c96-105">DESCRIPTION</span></span>
<span data-ttu-id="17c96-106">Этот Remove-AzSqlServerKeyVaultKey удаляет ключ сейфа с указанного SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="17c96-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="17c96-107">Обратите внимание SQL что разрешения сервера для хранилища ключа не меняются.</span><span class="sxs-lookup"><span data-stu-id="17c96-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="17c96-108">Чтобы изменить разрешения, используйте Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="17c96-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="17c96-109">Обратите внимание, что этот cmdlet не изменяет хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="17c96-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="17c96-110">Чтобы удалить ключ из key Vault, используйте Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="17c96-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="17c96-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17c96-111">EXAMPLES</span></span>

### <span data-ttu-id="17c96-112">Пример 1. Удаление ключа сейфа</span><span class="sxs-lookup"><span data-stu-id="17c96-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="17c96-113">Эта команда удаляет ключ сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="17c96-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="17c96-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 11223344556678899001122334455677889900 CreationDate: 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="17c96-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="17c96-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c96-115">PARAMETERS</span></span>

### <span data-ttu-id="17c96-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17c96-116">-AsJob</span></span>
<span data-ttu-id="17c96-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="17c96-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17c96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c96-118">-DefaultProfile</span></span>
<span data-ttu-id="17c96-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17c96-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17c96-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="17c96-120">-KeyId</span></span>
<span data-ttu-id="17c96-121">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="17c96-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="17c96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c96-122">-ResourceGroupName</span></span>
<span data-ttu-id="17c96-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="17c96-123">The name of the resource group</span></span>

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

### <span data-ttu-id="17c96-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="17c96-124">-ServerName</span></span>
<span data-ttu-id="17c96-125">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="17c96-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="17c96-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17c96-126">-Confirm</span></span>
<span data-ttu-id="17c96-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17c96-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17c96-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17c96-128">-WhatIf</span></span>
<span data-ttu-id="17c96-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17c96-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17c96-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17c96-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17c96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c96-131">CommonParameters</span></span>
<span data-ttu-id="17c96-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c96-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17c96-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c96-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17c96-134">INPUTS</span></span>

### <span data-ttu-id="17c96-135">System.String</span><span class="sxs-lookup"><span data-stu-id="17c96-135">System.String</span></span>

## <span data-ttu-id="17c96-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17c96-136">OUTPUTS</span></span>

### <span data-ttu-id="17c96-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="17c96-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="17c96-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17c96-138">NOTES</span></span>

## <span data-ttu-id="17c96-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17c96-139">RELATED LINKS</span></span>

[<span data-ttu-id="17c96-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="17c96-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
