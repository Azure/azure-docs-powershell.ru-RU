---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245205"
---
# <span data-ttu-id="5a1a4-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a1a4-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5a1a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1a4-103">Добавляет ключ хранилища ключей на сервер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="5a1a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a1a4-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a1a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a1a4-105">DESCRIPTION</span></span>
<span data-ttu-id="5a1a4-106">Командлет Add-AzSqlServerKeyVaultKey добавляет ключ хранилища ключей на указанный SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="5a1a4-107">У сервера должны быть разрешения "получить, wrapKey, unwrapKey" для хранилища.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="5a1a4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a1a4-108">EXAMPLES</span></span>

### <span data-ttu-id="5a1a4-109">Пример 1: Добавление ключа хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="5a1a4-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5a1a4-110">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoServer" в SQL Server в группе ресурсов "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="5a1a4-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="5a1a4-111">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="5a1a4-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5a1a4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a1a4-112">PARAMETERS</span></span>

### <span data-ttu-id="5a1a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a1a4-113">-AsJob</span></span>
<span data-ttu-id="5a1a4-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5a1a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a1a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1a4-115">-DefaultProfile</span></span>
<span data-ttu-id="5a1a4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a1a4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a1a4-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5a1a4-117">-KeyId</span></span>
<span data-ttu-id="5a1a4-118">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="5a1a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a1a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a1a4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-120">The name of the resource group</span></span>

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

### <span data-ttu-id="5a1a4-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5a1a4-121">-ServerName</span></span>
<span data-ttu-id="5a1a4-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5a1a4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a1a4-123">-Confirm</span></span>
<span data-ttu-id="5a1a4-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a1a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a1a4-125">-WhatIf</span></span>
<span data-ttu-id="5a1a4-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a1a4-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a1a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1a4-128">CommonParameters</span></span>
<span data-ttu-id="5a1a4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a1a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1a4-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a1a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1a4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a1a4-131">INPUTS</span></span>

### <span data-ttu-id="5a1a4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5a1a4-132">System.String</span></span>

## <span data-ttu-id="5a1a4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a1a4-133">OUTPUTS</span></span>

### <span data-ttu-id="5a1a4-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5a1a4-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5a1a4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a1a4-135">NOTES</span></span>

## <span data-ttu-id="5a1a4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a1a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a1a4-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5a1a4-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)