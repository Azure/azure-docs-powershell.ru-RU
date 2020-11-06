---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: c8b186c55161732a014e281162fa5d6131e72115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568129"
---
# <span data-ttu-id="134f0-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="134f0-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="134f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="134f0-102">SYNOPSIS</span></span>
<span data-ttu-id="134f0-103">Удаляет администратора Azure Active Directory для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="134f0-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="134f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="134f0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="134f0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="134f0-105">DESCRIPTION</span></span>
<span data-ttu-id="134f0-106">Командлет **Remove-AzureRmSqlServerActiveDirectoryAdministrator** удаляет администратора Azure Active Directory (Azure AD) для AzureSQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="134f0-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="134f0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="134f0-107">EXAMPLES</span></span>

### <span data-ttu-id="134f0-108">Пример 1: Удаление администратора</span><span class="sxs-lookup"><span data-stu-id="134f0-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="134f0-109">Эта команда удаляет администратора Azure Active Directory для сервера с именем Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="134f0-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="134f0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="134f0-110">PARAMETERS</span></span>

### <span data-ttu-id="134f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134f0-111">-DefaultProfile</span></span>
<span data-ttu-id="134f0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="134f0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="134f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="134f0-113">-Force</span></span>
<span data-ttu-id="134f0-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="134f0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="134f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="134f0-116">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="134f0-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="134f0-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="134f0-117">-ServerName</span></span>
<span data-ttu-id="134f0-118">Указывает имя сервера SQL Server, для которого этот командлет удаляет администратора.</span><span class="sxs-lookup"><span data-stu-id="134f0-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="134f0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="134f0-119">-Confirm</span></span>
<span data-ttu-id="134f0-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="134f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="134f0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="134f0-121">-WhatIf</span></span>
<span data-ttu-id="134f0-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="134f0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="134f0-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="134f0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="134f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134f0-124">CommonParameters</span></span>
<span data-ttu-id="134f0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="134f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134f0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="134f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134f0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="134f0-127">INPUTS</span></span>

### <span data-ttu-id="134f0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="134f0-128">System.String</span></span>

## <span data-ttu-id="134f0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="134f0-129">OUTPUTS</span></span>

### <span data-ttu-id="134f0-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="134f0-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="134f0-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="134f0-131">NOTES</span></span>

## <span data-ttu-id="134f0-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="134f0-132">RELATED LINKS</span></span>

[<span data-ttu-id="134f0-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="134f0-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="134f0-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="134f0-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="134f0-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="134f0-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


