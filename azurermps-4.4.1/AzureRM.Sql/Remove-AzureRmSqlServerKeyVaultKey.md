---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732185"
---
# <span data-ttu-id="4daad-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4daad-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="4daad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4daad-102">SYNOPSIS</span></span>
<span data-ttu-id="4daad-103">Удаление ключа хранилища ключей из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4daad-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4daad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4daad-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4daad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4daad-105">DESCRIPTION</span></span>
<span data-ttu-id="4daad-106">Командлет Remove-AzureRmSqlServerKeyVaultKey удаляет ключ хранилища ключей из указанного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4daad-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="4daad-107">Обратите внимание, что разрешения SQL Server для хранилища ключа не изменяются.</span><span class="sxs-lookup"><span data-stu-id="4daad-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="4daad-108">Чтобы изменить разрешения, используйте Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="4daad-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="4daad-109">Обратите внимание, что этот командлет не вносит изменения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4daad-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="4daad-110">Чтобы удалить раздел из хранилища ключей, используйте Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="4daad-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="4daad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4daad-111">EXAMPLES</span></span>

### <span data-ttu-id="4daad-112">--------------------------Пример 1: Удаление ключа хранилища ключей--------------------------</span><span class="sxs-lookup"><span data-stu-id="4daad-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="4daad-113">Эта команда удаляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="4daad-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="4daad-114">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="4daad-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="4daad-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4daad-115">PARAMETERS</span></span>

### <span data-ttu-id="4daad-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4daad-116">-KeyId</span></span>
<span data-ttu-id="4daad-117">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="4daad-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="4daad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4daad-118">-ResourceGroupName</span></span>
<span data-ttu-id="4daad-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4daad-119">The name of the resource group</span></span>

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

### <span data-ttu-id="4daad-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4daad-120">-ServerName</span></span>
<span data-ttu-id="4daad-121">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4daad-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4daad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4daad-122">-Confirm</span></span>
<span data-ttu-id="4daad-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4daad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4daad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4daad-124">-WhatIf</span></span>
<span data-ttu-id="4daad-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4daad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4daad-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4daad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4daad-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4daad-127">-DefaultProfile</span></span>
<span data-ttu-id="4daad-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4daad-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4daad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4daad-129">CommonParameters</span></span>
<span data-ttu-id="4daad-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4daad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4daad-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4daad-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4daad-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4daad-132">INPUTS</span></span>

### <span data-ttu-id="4daad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4daad-133">System.String</span></span>

## <span data-ttu-id="4daad-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4daad-134">OUTPUTS</span></span>

### <span data-ttu-id="4daad-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="4daad-135">System.Object</span></span>

## <span data-ttu-id="4daad-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4daad-136">NOTES</span></span>

## <span data-ttu-id="4daad-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4daad-137">RELATED LINKS</span></span>

[<span data-ttu-id="4daad-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4daad-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
