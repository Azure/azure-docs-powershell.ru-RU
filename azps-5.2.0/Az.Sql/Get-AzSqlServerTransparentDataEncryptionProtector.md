---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401860"
---
# <span data-ttu-id="71f97-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71f97-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="71f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71f97-102">SYNOPSIS</span></span>
<span data-ttu-id="71f97-103">Получает прозрачный защита шифрования данных (TDE)</span><span class="sxs-lookup"><span data-stu-id="71f97-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="71f97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71f97-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f97-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71f97-105">DESCRIPTION</span></span>
<span data-ttu-id="71f97-106">Этот Get-AzSqlServerTransparentDataEncryptionProtector получает сведения о защите TDE.</span><span class="sxs-lookup"><span data-stu-id="71f97-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="71f97-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71f97-107">EXAMPLES</span></span>

### <span data-ttu-id="71f97-108">Пример 1. Защита прозрачного шифрования данных (TDE)</span><span class="sxs-lookup"><span data-stu-id="71f97-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="71f97-109">Эта команда получает защиту TDE для сервера ContosoServer в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71f97-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="71f97-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="71f97-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="71f97-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="71f97-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="71f97-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71f97-112">PARAMETERS</span></span>

### <span data-ttu-id="71f97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f97-113">-DefaultProfile</span></span>
<span data-ttu-id="71f97-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71f97-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71f97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f97-115">-ResourceGroupName</span></span>
<span data-ttu-id="71f97-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="71f97-116">The name of the resource group</span></span>

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

### <span data-ttu-id="71f97-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71f97-117">-ServerName</span></span>
<span data-ttu-id="71f97-118">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="71f97-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="71f97-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71f97-119">-Confirm</span></span>
<span data-ttu-id="71f97-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71f97-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f97-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f97-121">-WhatIf</span></span>
<span data-ttu-id="71f97-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71f97-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f97-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71f97-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f97-124">CommonParameters</span></span>
<span data-ttu-id="71f97-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f97-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71f97-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f97-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71f97-127">INPUTS</span></span>

### <span data-ttu-id="71f97-128">System.String</span><span class="sxs-lookup"><span data-stu-id="71f97-128">System.String</span></span>

## <span data-ttu-id="71f97-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71f97-129">OUTPUTS</span></span>

### <span data-ttu-id="71f97-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="71f97-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="71f97-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71f97-131">NOTES</span></span>

## <span data-ttu-id="71f97-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71f97-132">RELATED LINKS</span></span>

[<span data-ttu-id="71f97-133">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="71f97-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
