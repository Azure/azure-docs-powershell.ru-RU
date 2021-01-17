---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419036"
---
# <span data-ttu-id="e178e-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e178e-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e178e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e178e-102">SYNOPSIS</span></span>
<span data-ttu-id="e178e-103">Удаляет администратора Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e178e-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="e178e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e178e-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e178e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e178e-105">DESCRIPTION</span></span>
<span data-ttu-id="e178e-106">Для **AzureSQL** Server в текущей подписке удаляется администратор Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e178e-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="e178e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e178e-107">EXAMPLES</span></span>

### <span data-ttu-id="e178e-108">Пример 1. Удаление администратора</span><span class="sxs-lookup"><span data-stu-id="e178e-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e178e-109">Эта команда удаляет администратор Azure AD для сервера Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e178e-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e178e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e178e-110">PARAMETERS</span></span>

### <span data-ttu-id="e178e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e178e-111">-DefaultProfile</span></span>
<span data-ttu-id="e178e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e178e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e178e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e178e-113">-Force</span></span>
<span data-ttu-id="e178e-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e178e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e178e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e178e-115">-ResourceGroupName</span></span>
<span data-ttu-id="e178e-116">Имя группы ресурсов, которой назначена SQL Server ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e178e-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="e178e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e178e-117">-ServerName</span></span>
<span data-ttu-id="e178e-118">Указывает имя учетной записи SQL Server для которой этот cmdlet удаляет администратора.</span><span class="sxs-lookup"><span data-stu-id="e178e-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="e178e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e178e-119">-Confirm</span></span>
<span data-ttu-id="e178e-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e178e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e178e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e178e-121">-WhatIf</span></span>
<span data-ttu-id="e178e-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e178e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e178e-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e178e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e178e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e178e-124">CommonParameters</span></span>
<span data-ttu-id="e178e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e178e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e178e-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e178e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e178e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e178e-127">INPUTS</span></span>

### <span data-ttu-id="e178e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e178e-128">System.String</span></span>

## <span data-ttu-id="e178e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e178e-129">OUTPUTS</span></span>

### <span data-ttu-id="e178e-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e178e-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e178e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e178e-131">NOTES</span></span>

## <span data-ttu-id="e178e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e178e-132">RELATED LINKS</span></span>

[<span data-ttu-id="e178e-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e178e-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e178e-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e178e-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e178e-135">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e178e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


