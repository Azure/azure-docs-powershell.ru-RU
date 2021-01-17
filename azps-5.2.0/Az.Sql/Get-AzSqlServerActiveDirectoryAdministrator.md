---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404527"
---
# <span data-ttu-id="aa55a-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa55a-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="aa55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa55a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa55a-103">Сведения о администраторе Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa55a-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="aa55a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa55a-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa55a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa55a-105">DESCRIPTION</span></span>
<span data-ttu-id="aa55a-106">Чтобы получить сведения об администраторе Azure Active Directory (Azure AD) для AzureSQL Server в текущей подписке, можно получить сведения об администраторе **Get-AzSqlServerActiveDirectoryAdministrator.**</span><span class="sxs-lookup"><span data-stu-id="aa55a-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="aa55a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa55a-107">EXAMPLES</span></span>

### <span data-ttu-id="aa55a-108">Пример 1. Получает сведения об администраторе сервера</span><span class="sxs-lookup"><span data-stu-id="aa55a-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="aa55a-109">Эта команда получает сведения о администраторе Azure AD для сервера Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="aa55a-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="aa55a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa55a-110">PARAMETERS</span></span>

### <span data-ttu-id="aa55a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa55a-111">-DefaultProfile</span></span>
<span data-ttu-id="aa55a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa55a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa55a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa55a-113">-ResourceGroupName</span></span>
<span data-ttu-id="aa55a-114">Имя группы ресурсов, которой назначена SQL Server ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa55a-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="aa55a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa55a-115">-ServerName</span></span>
<span data-ttu-id="aa55a-116">Определяет имя SQL Server, для которого этот cmdlet получает сведения.</span><span class="sxs-lookup"><span data-stu-id="aa55a-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="aa55a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa55a-117">-Confirm</span></span>
<span data-ttu-id="aa55a-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa55a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa55a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa55a-119">-WhatIf</span></span>
<span data-ttu-id="aa55a-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa55a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa55a-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa55a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa55a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa55a-122">CommonParameters</span></span>
<span data-ttu-id="aa55a-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa55a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa55a-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa55a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa55a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa55a-125">INPUTS</span></span>

### <span data-ttu-id="aa55a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="aa55a-126">System.String</span></span>

## <span data-ttu-id="aa55a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa55a-127">OUTPUTS</span></span>

### <span data-ttu-id="aa55a-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="aa55a-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="aa55a-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa55a-129">NOTES</span></span>

## <span data-ttu-id="aa55a-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa55a-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa55a-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa55a-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="aa55a-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa55a-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="aa55a-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="aa55a-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="aa55a-134">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="aa55a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


