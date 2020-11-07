---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729080"
---
# <span data-ttu-id="d6796-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6796-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="d6796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6796-102">SYNOPSIS</span></span>
<span data-ttu-id="d6796-103">Добавляет ключ хранилища ключей на сервер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6796-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="d6796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6796-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6796-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6796-105">DESCRIPTION</span></span>
<span data-ttu-id="d6796-106">Командлет Add-AzSqlServerKeyVaultKey добавляет ключ хранилища ключей на указанный SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6796-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="d6796-107">У сервера должны быть разрешения "получить, wrapKey, unwrapKey" для хранилища.</span><span class="sxs-lookup"><span data-stu-id="d6796-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="d6796-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6796-108">EXAMPLES</span></span>

### <span data-ttu-id="d6796-109">Пример 1: Добавление ключа хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="d6796-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d6796-110">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoServer" в SQL Server в группе ресурсов "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d6796-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="d6796-111">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="d6796-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="d6796-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6796-112">PARAMETERS</span></span>

### <span data-ttu-id="d6796-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6796-113">-AsJob</span></span>
<span data-ttu-id="d6796-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d6796-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6796-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6796-115">-DefaultProfile</span></span>
<span data-ttu-id="d6796-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d6796-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6796-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d6796-117">-KeyId</span></span>
<span data-ttu-id="d6796-118">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="d6796-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="d6796-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6796-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6796-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6796-120">The name of the resource group</span></span>

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

### <span data-ttu-id="d6796-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d6796-121">-ServerName</span></span>
<span data-ttu-id="d6796-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d6796-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d6796-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6796-123">-Confirm</span></span>
<span data-ttu-id="d6796-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6796-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6796-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6796-125">-WhatIf</span></span>
<span data-ttu-id="d6796-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6796-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6796-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6796-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6796-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6796-128">CommonParameters</span></span>
<span data-ttu-id="d6796-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6796-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6796-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6796-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6796-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6796-131">INPUTS</span></span>

### <span data-ttu-id="d6796-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6796-132">System.String</span></span>

## <span data-ttu-id="d6796-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6796-133">OUTPUTS</span></span>

### <span data-ttu-id="d6796-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="d6796-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="d6796-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6796-135">NOTES</span></span>

## <span data-ttu-id="d6796-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6796-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6796-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d6796-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
