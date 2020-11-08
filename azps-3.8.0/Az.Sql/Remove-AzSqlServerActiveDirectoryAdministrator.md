---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072939"
---
# <span data-ttu-id="1eace-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1eace-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="1eace-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eace-102">SYNOPSIS</span></span>
<span data-ttu-id="1eace-103">Удаляет администратора Azure Active Directory для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1eace-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="1eace-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eace-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eace-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eace-105">DESCRIPTION</span></span>
<span data-ttu-id="1eace-106">Командлет **Remove-AzSqlServerActiveDirectoryAdministrator** удаляет администратора Azure Active Directory (Azure AD) для AzureSQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1eace-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="1eace-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eace-107">EXAMPLES</span></span>

### <span data-ttu-id="1eace-108">Пример 1: Удаление администратора</span><span class="sxs-lookup"><span data-stu-id="1eace-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="1eace-109">Эта команда удаляет администратора Azure Active Directory для сервера с именем Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1eace-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="1eace-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eace-110">PARAMETERS</span></span>

### <span data-ttu-id="1eace-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eace-111">-DefaultProfile</span></span>
<span data-ttu-id="1eace-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1eace-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eace-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1eace-113">-Force</span></span>
<span data-ttu-id="1eace-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1eace-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1eace-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eace-115">-ResourceGroupName</span></span>
<span data-ttu-id="1eace-116">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1eace-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="1eace-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1eace-117">-ServerName</span></span>
<span data-ttu-id="1eace-118">Указывает имя сервера SQL Server, для которого этот командлет удаляет администратора.</span><span class="sxs-lookup"><span data-stu-id="1eace-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="1eace-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eace-119">-Confirm</span></span>
<span data-ttu-id="1eace-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1eace-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eace-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eace-121">-WhatIf</span></span>
<span data-ttu-id="1eace-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1eace-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eace-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1eace-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eace-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eace-124">CommonParameters</span></span>
<span data-ttu-id="1eace-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eace-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eace-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eace-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eace-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eace-127">INPUTS</span></span>

### <span data-ttu-id="1eace-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1eace-128">System.String</span></span>

## <span data-ttu-id="1eace-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eace-129">OUTPUTS</span></span>

### <span data-ttu-id="1eace-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="1eace-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="1eace-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eace-131">NOTES</span></span>

## <span data-ttu-id="1eace-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eace-132">RELATED LINKS</span></span>

[<span data-ttu-id="1eace-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1eace-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="1eace-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1eace-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="1eace-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1eace-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


