---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561443"
---
# <span data-ttu-id="d9c0c-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9c0c-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d9c0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c0c-103">Получение сведений о администраторе Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9c0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9c0c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c0c-106">Командлет **Get-AzureRmSqlServerActiveDirectoryAdministrator** получает сведения об администраторе Azure Active Directory (Azure AD) для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="d9c0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9c0c-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c0c-108">Пример 1: получение сведений о администраторе сервера</span><span class="sxs-lookup"><span data-stu-id="d9c0c-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="d9c0c-109">Эта команда получает сведения о администраторе Azure Active Directory для сервера с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d9c0c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="d9c0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c0c-111">-DefaultProfile</span></span>
<span data-ttu-id="d9c0c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9c0c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c0c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c0c-113">-ResourceGroupName</span></span>
<span data-ttu-id="d9c0c-114">Указывает имя группы ресурсов, которой назначен SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c0c-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d9c0c-115">-ServerName</span></span>
<span data-ttu-id="d9c0c-116">Указывает имя сервера SQL Server, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c0c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9c0c-117">-Confirm</span></span>
<span data-ttu-id="d9c0c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c0c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c0c-119">-WhatIf</span></span>
<span data-ttu-id="d9c0c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c0c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c0c-122">CommonParameters</span></span>
<span data-ttu-id="d9c0c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c0c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c0c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c0c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9c0c-125">INPUTS</span></span>

### <span data-ttu-id="d9c0c-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="d9c0c-126">None</span></span>
<span data-ttu-id="d9c0c-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d9c0c-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9c0c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9c0c-128">OUTPUTS</span></span>

### <span data-ttu-id="d9c0c-129">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="d9c0c-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="d9c0c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9c0c-130">NOTES</span></span>

## <span data-ttu-id="d9c0c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9c0c-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9c0c-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9c0c-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d9c0c-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9c0c-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d9c0c-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d9c0c-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


