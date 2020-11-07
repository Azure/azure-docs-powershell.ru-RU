---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 333e4b1e5f01c76947ca32277fd8ca7ff75218eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732347"
---
# <span data-ttu-id="90dc3-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90dc3-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="90dc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="90dc3-103">Удаление ключа хранилища ключей из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90dc3-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90dc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90dc3-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90dc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="90dc3-106">Командлет Remove-AzureRmSqlServerKeyVaultKey удаляет ключ хранилища ключей из указанного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90dc3-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="90dc3-107">Обратите внимание, что разрешения SQL Server для хранилища ключа не изменяются.</span><span class="sxs-lookup"><span data-stu-id="90dc3-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="90dc3-108">Чтобы изменить разрешения, используйте Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="90dc3-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="90dc3-109">Обратите внимание, что этот командлет не вносит изменения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="90dc3-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="90dc3-110">Чтобы удалить раздел из хранилища ключей, используйте Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="90dc3-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="90dc3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90dc3-111">EXAMPLES</span></span>

### <span data-ttu-id="90dc3-112">Пример 1: Удаление ключа хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="90dc3-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="90dc3-113">Эта команда удаляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="90dc3-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="90dc3-114">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="90dc3-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="90dc3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90dc3-115">PARAMETERS</span></span>

### <span data-ttu-id="90dc3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90dc3-116">-AsJob</span></span>
<span data-ttu-id="90dc3-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="90dc3-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dc3-118">-DefaultProfile</span></span>
<span data-ttu-id="90dc3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="90dc3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="90dc3-120">-KeyId</span></span>
<span data-ttu-id="90dc3-121">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="90dc3-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90dc3-122">-ResourceGroupName</span></span>
<span data-ttu-id="90dc3-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90dc3-123">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="90dc3-124">-ServerName</span></span>
<span data-ttu-id="90dc3-125">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90dc3-125">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90dc3-126">-Confirm</span></span>
<span data-ttu-id="90dc3-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90dc3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dc3-128">-WhatIf</span></span>
<span data-ttu-id="90dc3-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90dc3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dc3-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90dc3-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dc3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dc3-131">CommonParameters</span></span>
<span data-ttu-id="90dc3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90dc3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dc3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90dc3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dc3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90dc3-134">INPUTS</span></span>

### <span data-ttu-id="90dc3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="90dc3-135">System.String</span></span>

## <span data-ttu-id="90dc3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90dc3-136">OUTPUTS</span></span>

### <span data-ttu-id="90dc3-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="90dc3-137">System.Object</span></span>

## <span data-ttu-id="90dc3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="90dc3-138">NOTES</span></span>

## <span data-ttu-id="90dc3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90dc3-139">RELATED LINKS</span></span>

[<span data-ttu-id="90dc3-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="90dc3-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
