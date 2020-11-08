---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073702"
---
# <span data-ttu-id="f5cf5-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5cf5-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f5cf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cf5-103">Возвращает ключи хранилища ключей SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="f5cf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5cf5-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5cf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f5cf5-106">Командлет Get-AzSqlServerKeyVaultKey получает сведения о ключах хранилища ключей на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="f5cf5-107">Вы можете просмотреть все клавиши на сервере или просмотреть определенную клавишу, предоставив KeyId.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="f5cf5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5cf5-108">EXAMPLES</span></span>

### <span data-ttu-id="f5cf5-109">Пример 1: получение всех ключей хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="f5cf5-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f5cf5-110">Эта команда получает все ключи хранилища ключей на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="f5cf5-111">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="f5cf5-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="f5cf5-112">Пример 2: получение ключа хранилища с определенным ключом</span><span class="sxs-lookup"><span data-stu-id="f5cf5-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f5cf5-113">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ", а затем сохраняет его в переменной $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="f5cf5-114">Вы можете узнать о свойствах $MyServerKeyVaultKey, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="f5cf5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5cf5-115">PARAMETERS</span></span>

### <span data-ttu-id="f5cf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cf5-116">-DefaultProfile</span></span>
<span data-ttu-id="f5cf5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5cf5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5cf5-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f5cf5-118">-KeyId</span></span>
<span data-ttu-id="f5cf5-119">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cf5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cf5-120">-ResourceGroupName</span></span>
<span data-ttu-id="f5cf5-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-121">The name of the resource group</span></span>

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

### <span data-ttu-id="f5cf5-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f5cf5-122">-ServerName</span></span>
<span data-ttu-id="f5cf5-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f5cf5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5cf5-124">-Confirm</span></span>
<span data-ttu-id="f5cf5-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5cf5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cf5-126">-WhatIf</span></span>
<span data-ttu-id="f5cf5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5cf5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5cf5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cf5-129">CommonParameters</span></span>
<span data-ttu-id="f5cf5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5cf5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cf5-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5cf5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cf5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5cf5-132">INPUTS</span></span>

### <span data-ttu-id="f5cf5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f5cf5-133">System.String</span></span>

## <span data-ttu-id="f5cf5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5cf5-134">OUTPUTS</span></span>

### <span data-ttu-id="f5cf5-135">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f5cf5-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f5cf5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5cf5-136">NOTES</span></span>

## <span data-ttu-id="f5cf5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5cf5-137">RELATED LINKS</span></span>

[<span data-ttu-id="f5cf5-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f5cf5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
