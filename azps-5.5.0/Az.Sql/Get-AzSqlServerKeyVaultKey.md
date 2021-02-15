---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235564"
---
# <span data-ttu-id="d6732-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6732-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="d6732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6732-102">SYNOPSIS</span></span>
<span data-ttu-id="d6732-103">Возвращает ключ SQL ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="d6732-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="d6732-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6732-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6732-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6732-105">DESCRIPTION</span></span>
<span data-ttu-id="d6732-106">Этот Get-AzSqlServerKeyVaultKey получает сведения о ключах сейфа на SQL сервере.</span><span class="sxs-lookup"><span data-stu-id="d6732-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d6732-107">Вы можете просмотреть все ключи на сервере или определенный ключ, задав keyId.</span><span class="sxs-lookup"><span data-stu-id="d6732-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="d6732-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6732-108">EXAMPLES</span></span>

### <span data-ttu-id="d6732-109">Пример 1. Получить все клавиши key Vault</span><span class="sxs-lookup"><span data-stu-id="d6732-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d6732-110">Эта команда получает все клавиши ключевых сейфов на SQL сервере.</span><span class="sxs-lookup"><span data-stu-id="d6732-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="d6732-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate: 01.01.2017 12:00:00GroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type : AzureKeyVault Uri https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 : Thumbprint : 00998877665544332211009887766554433211 CreationDate: 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="d6732-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="d6732-112">Пример 2. Получить определенный ключ сейфа</span><span class="sxs-lookup"><span data-stu-id="d6732-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d6732-113">Эта команда получает ключ сейфа с ИД ', а затем сохраняет его в https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 $MyServerKeyVaultKey переменной.</span><span class="sxs-lookup"><span data-stu-id="d6732-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="d6732-114">Вы можете проверить свойства $MyServerKeyVaultKey, чтобы получить подробные сведения о хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="d6732-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="d6732-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6732-115">PARAMETERS</span></span>

### <span data-ttu-id="d6732-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6732-116">-DefaultProfile</span></span>
<span data-ttu-id="d6732-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d6732-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6732-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d6732-118">-KeyId</span></span>
<span data-ttu-id="d6732-119">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="d6732-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="d6732-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6732-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6732-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6732-121">The name of the resource group</span></span>

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

### <span data-ttu-id="d6732-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6732-122">-ServerName</span></span>
<span data-ttu-id="d6732-123">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d6732-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d6732-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6732-124">-Confirm</span></span>
<span data-ttu-id="d6732-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d6732-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6732-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6732-126">-WhatIf</span></span>
<span data-ttu-id="d6732-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6732-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6732-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6732-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6732-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6732-129">CommonParameters</span></span>
<span data-ttu-id="d6732-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6732-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6732-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6732-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6732-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6732-132">INPUTS</span></span>

### <span data-ttu-id="d6732-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d6732-133">System.String</span></span>

## <span data-ttu-id="d6732-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6732-134">OUTPUTS</span></span>

### <span data-ttu-id="d6732-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="d6732-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="d6732-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6732-136">NOTES</span></span>

## <span data-ttu-id="d6732-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6732-137">RELATED LINKS</span></span>

[<span data-ttu-id="d6732-138">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d6732-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
