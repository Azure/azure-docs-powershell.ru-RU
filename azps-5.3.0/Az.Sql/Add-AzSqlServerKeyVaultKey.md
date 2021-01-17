---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419671"
---
# <span data-ttu-id="9dee2-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9dee2-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="9dee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dee2-102">SYNOPSIS</span></span>
<span data-ttu-id="9dee2-103">Добавляет ключ сейфа к SQL серверу.</span><span class="sxs-lookup"><span data-stu-id="9dee2-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="9dee2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9dee2-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dee2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dee2-105">DESCRIPTION</span></span>
<span data-ttu-id="9dee2-106">Этот Add-AzSqlServerKeyVaultKey добавляет ключ сейфа к предоставленной SQL серверу.</span><span class="sxs-lookup"><span data-stu-id="9dee2-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="9dee2-107">У сервера должны быть разрешения на доступ к хранилищу .</span><span class="sxs-lookup"><span data-stu-id="9dee2-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="9dee2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9dee2-108">EXAMPLES</span></span>

### <span data-ttu-id="9dee2-109">Пример 1. Добавление ключа сейфа</span><span class="sxs-lookup"><span data-stu-id="9dee2-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="9dee2-110">Эта команда добавляет ключ сейфа с ИД ' на SQL-сервер https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoServer в группе ресурсов "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="9dee2-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="9dee2-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122334455667788990011223344556677889900 CreationDate: 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9dee2-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="9dee2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dee2-112">PARAMETERS</span></span>

### <span data-ttu-id="9dee2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dee2-113">-AsJob</span></span>
<span data-ttu-id="9dee2-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9dee2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dee2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dee2-115">-DefaultProfile</span></span>
<span data-ttu-id="9dee2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9dee2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dee2-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="9dee2-117">-KeyId</span></span>
<span data-ttu-id="9dee2-118">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="9dee2-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="9dee2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dee2-119">-ResourceGroupName</span></span>
<span data-ttu-id="9dee2-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9dee2-120">The name of the resource group</span></span>

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

### <span data-ttu-id="9dee2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9dee2-121">-ServerName</span></span>
<span data-ttu-id="9dee2-122">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="9dee2-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9dee2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dee2-123">-Confirm</span></span>
<span data-ttu-id="9dee2-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dee2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dee2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dee2-125">-WhatIf</span></span>
<span data-ttu-id="9dee2-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dee2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dee2-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9dee2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dee2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dee2-128">CommonParameters</span></span>
<span data-ttu-id="9dee2-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dee2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dee2-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dee2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dee2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dee2-131">INPUTS</span></span>

### <span data-ttu-id="9dee2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9dee2-132">System.String</span></span>

## <span data-ttu-id="9dee2-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9dee2-133">OUTPUTS</span></span>

### <span data-ttu-id="9dee2-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="9dee2-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="9dee2-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9dee2-135">NOTES</span></span>

## <span data-ttu-id="9dee2-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dee2-136">RELATED LINKS</span></span>

[<span data-ttu-id="9dee2-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="9dee2-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
