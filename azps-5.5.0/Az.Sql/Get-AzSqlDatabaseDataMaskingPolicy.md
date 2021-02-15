---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211057"
---
# <span data-ttu-id="c4623-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4623-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="c4623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4623-102">SYNOPSIS</span></span>
<span data-ttu-id="c4623-103">Возвращает политику маскровки данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="c4623-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4623-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4623-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4623-105">DESCRIPTION</span></span>
<span data-ttu-id="c4623-106">Для **этого к** базе данных Azure SQL политики маскровки данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="c4623-107">Чтобы использовать этот cmdlet, используйте параметры *ResourceGroupName,* *ServerName* и *DatabaseName* для определения базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c4623-108">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="c4623-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c4623-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4623-109">EXAMPLES</span></span>

### <span data-ttu-id="c4623-110">Пример 1. Просмотр политики маскровки данных для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="c4623-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="c4623-111">Эта команда получает политику маскровки данных из базы данных Database01 в группе ресурсов ResourceGroup01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="c4623-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="c4623-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4623-112">PARAMETERS</span></span>

### <span data-ttu-id="c4623-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4623-113">-DatabaseName</span></span>
<span data-ttu-id="c4623-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c4623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4623-115">-DefaultProfile</span></span>
<span data-ttu-id="c4623-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4623-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4623-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4623-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4623-118">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c4623-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4623-119">-ServerName</span></span>
<span data-ttu-id="c4623-120">Указывает имя сервера, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="c4623-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="c4623-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4623-121">-Confirm</span></span>
<span data-ttu-id="c4623-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4623-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4623-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4623-123">-WhatIf</span></span>
<span data-ttu-id="c4623-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4623-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4623-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4623-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4623-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4623-126">CommonParameters</span></span>
<span data-ttu-id="c4623-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4623-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4623-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4623-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4623-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4623-129">INPUTS</span></span>

### <span data-ttu-id="c4623-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c4623-130">System.String</span></span>

## <span data-ttu-id="c4623-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4623-131">OUTPUTS</span></span>

### <span data-ttu-id="c4623-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c4623-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="c4623-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4623-133">NOTES</span></span>

## <span data-ttu-id="c4623-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4623-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4623-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c4623-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c4623-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c4623-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c4623-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c4623-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c4623-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4623-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="c4623-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c4623-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


