---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066946"
---
# <span data-ttu-id="3a081-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3a081-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="3a081-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a081-102">SYNOPSIS</span></span>
<span data-ttu-id="3a081-103">Получение сведений о администраторе Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a081-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="3a081-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a081-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a081-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a081-105">DESCRIPTION</span></span>
<span data-ttu-id="3a081-106">Командлет **Get-AzSqlServerActiveDirectoryAdministrator** получает сведения об администраторе Azure Active Directory (Azure AD) для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="3a081-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3a081-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a081-107">EXAMPLES</span></span>

### <span data-ttu-id="3a081-108">Пример 1: получение сведений о администраторе сервера</span><span class="sxs-lookup"><span data-stu-id="3a081-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="3a081-109">Эта команда получает сведения о администраторе Azure Active Directory для сервера с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3a081-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3a081-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a081-110">PARAMETERS</span></span>

### <span data-ttu-id="3a081-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a081-111">-DefaultProfile</span></span>
<span data-ttu-id="3a081-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a081-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a081-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a081-113">-ResourceGroupName</span></span>
<span data-ttu-id="3a081-114">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a081-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="3a081-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3a081-115">-ServerName</span></span>
<span data-ttu-id="3a081-116">Указывает имя сервера SQL Server, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="3a081-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="3a081-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a081-117">-Confirm</span></span>
<span data-ttu-id="3a081-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a081-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a081-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a081-119">-WhatIf</span></span>
<span data-ttu-id="3a081-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a081-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a081-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a081-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a081-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a081-122">CommonParameters</span></span>
<span data-ttu-id="3a081-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a081-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a081-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a081-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a081-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a081-125">INPUTS</span></span>

### <span data-ttu-id="3a081-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3a081-126">System.String</span></span>

## <span data-ttu-id="3a081-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a081-127">OUTPUTS</span></span>

### <span data-ttu-id="3a081-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="3a081-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="3a081-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a081-129">NOTES</span></span>

## <span data-ttu-id="3a081-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a081-130">RELATED LINKS</span></span>

[<span data-ttu-id="3a081-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3a081-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3a081-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3a081-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3a081-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3a081-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3a081-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3a081-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


