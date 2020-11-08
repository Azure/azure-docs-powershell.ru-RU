---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066487"
---
# <span data-ttu-id="0c0dd-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0c0dd-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="0c0dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0dd-103">Отключение проверки подлинности Azure AD для определенного сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="0c0dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c0dd-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c0dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c0dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0dd-106">Командлет **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="0c0dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c0dd-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c0dd-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="0c0dd-109">Эта команда отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для сервера AzureSQL с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0c0dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c0dd-110">PARAMETERS</span></span>

### <span data-ttu-id="0c0dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0dd-111">-DefaultProfile</span></span>
<span data-ttu-id="0c0dd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0dd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0dd-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c0dd-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c0dd-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0c0dd-115">-ServerName</span></span>
<span data-ttu-id="0c0dd-116">Имя сервера Azure SQL Server, в котором находится администратор Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="0c0dd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c0dd-117">-Confirm</span></span>
<span data-ttu-id="0c0dd-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0dd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0dd-119">-WhatIf</span></span>
<span data-ttu-id="0c0dd-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c0dd-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c0dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0dd-122">CommonParameters</span></span>
<span data-ttu-id="0c0dd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c0dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0dd-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c0dd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0dd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c0dd-125">INPUTS</span></span>

### <span data-ttu-id="0c0dd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0c0dd-126">System.String</span></span>

## <span data-ttu-id="0c0dd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c0dd-127">OUTPUTS</span></span>

### <span data-ttu-id="0c0dd-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="0c0dd-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="0c0dd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c0dd-129">NOTES</span></span>

## <span data-ttu-id="0c0dd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c0dd-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c0dd-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0c0dd-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0c0dd-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0c0dd-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0c0dd-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0c0dd-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0c0dd-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="0c0dd-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
