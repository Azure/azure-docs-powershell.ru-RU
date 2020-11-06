---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ebd1fa17bfe35a4f0cb73d5ff3c3658e439abf78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565115"
---
# <span data-ttu-id="5d00f-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5d00f-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="5d00f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d00f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d00f-103">Получение сведений о администраторе Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5d00f-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d00f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d00f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d00f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d00f-105">DESCRIPTION</span></span>
<span data-ttu-id="5d00f-106">Командлет **Get-AzureRmSqlServerActiveDirectoryAdministrator** получает сведения об администраторе Azure Active Directory (Azure AD) для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="5d00f-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="5d00f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d00f-107">EXAMPLES</span></span>

### <span data-ttu-id="5d00f-108">Пример 1: получение сведений о администраторе сервера</span><span class="sxs-lookup"><span data-stu-id="5d00f-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="5d00f-109">Эта команда получает сведения о администраторе Azure Active Directory для сервера с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5d00f-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5d00f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d00f-110">PARAMETERS</span></span>

### <span data-ttu-id="5d00f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d00f-111">-ResourceGroupName</span></span>
<span data-ttu-id="5d00f-112">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5d00f-112">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5d00f-113">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5d00f-113">-ServerName</span></span>
<span data-ttu-id="5d00f-114">Указывает имя сервера SQL Server, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="5d00f-114">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="5d00f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d00f-115">-Confirm</span></span>
<span data-ttu-id="5d00f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d00f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d00f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d00f-117">-WhatIf</span></span>
<span data-ttu-id="5d00f-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d00f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d00f-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d00f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d00f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d00f-120">-DefaultProfile</span></span>
<span data-ttu-id="5d00f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d00f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d00f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d00f-122">CommonParameters</span></span>
<span data-ttu-id="5d00f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d00f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d00f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d00f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d00f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d00f-125">INPUTS</span></span>

## <span data-ttu-id="5d00f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d00f-126">OUTPUTS</span></span>

### <span data-ttu-id="5d00f-127">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="5d00f-127">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="5d00f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d00f-128">NOTES</span></span>

## <span data-ttu-id="5d00f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d00f-129">RELATED LINKS</span></span>

[<span data-ttu-id="5d00f-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5d00f-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5d00f-131">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5d00f-131">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5d00f-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5d00f-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


