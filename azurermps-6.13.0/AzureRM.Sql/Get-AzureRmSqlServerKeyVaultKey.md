---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 74d1909bee5eb4d2645fa1d25a429d1bc66d9f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568148"
---
# <span data-ttu-id="c87ec-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c87ec-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="c87ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c87ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c87ec-103">Возвращает ключи хранилища ключей SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c87ec-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c87ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c87ec-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ec-105">DESCRIPTION</span></span>
<span data-ttu-id="c87ec-106">Командлет Get-AzureRmSqlServerKeyVaultKey получает сведения о ключах хранилища ключей на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c87ec-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="c87ec-107">Вы можете просмотреть все клавиши на сервере или просмотреть определенную клавишу, предоставив KeyId.</span><span class="sxs-lookup"><span data-stu-id="c87ec-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="c87ec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c87ec-108">EXAMPLES</span></span>

### <span data-ttu-id="c87ec-109">Пример 1: получение всех ключей хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="c87ec-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c87ec-110">Эта команда получает все ключи хранилища ключей на сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c87ec-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="c87ec-111">ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 тип: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM ResourceGroupName: ContosoResourceGroup ИмяСервера: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="c87ec-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="c87ec-112">Пример 2: получение ключа хранилища с определенным ключом</span><span class="sxs-lookup"><span data-stu-id="c87ec-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c87ec-113">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ", а затем сохраняет его в переменной $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="c87ec-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="c87ec-114">Вы можете узнать о свойствах $MyServerKeyVaultKey, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="c87ec-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="c87ec-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c87ec-115">PARAMETERS</span></span>

### <span data-ttu-id="c87ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87ec-116">-DefaultProfile</span></span>
<span data-ttu-id="c87ec-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c87ec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c87ec-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c87ec-118">-KeyId</span></span>
<span data-ttu-id="c87ec-119">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="c87ec-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c87ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="c87ec-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c87ec-121">The name of the resource group</span></span>

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

### <span data-ttu-id="c87ec-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c87ec-122">-ServerName</span></span>
<span data-ttu-id="c87ec-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c87ec-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c87ec-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c87ec-124">-Confirm</span></span>
<span data-ttu-id="c87ec-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c87ec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87ec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87ec-126">-WhatIf</span></span>
<span data-ttu-id="c87ec-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c87ec-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87ec-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c87ec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87ec-129">CommonParameters</span></span>
<span data-ttu-id="c87ec-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c87ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87ec-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87ec-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87ec-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c87ec-132">INPUTS</span></span>

### <span data-ttu-id="c87ec-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c87ec-133">System.String</span></span>

## <span data-ttu-id="c87ec-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ec-134">OUTPUTS</span></span>

### <span data-ttu-id="c87ec-135">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="c87ec-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="c87ec-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c87ec-136">NOTES</span></span>

## <span data-ttu-id="c87ec-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c87ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="c87ec-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="c87ec-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
