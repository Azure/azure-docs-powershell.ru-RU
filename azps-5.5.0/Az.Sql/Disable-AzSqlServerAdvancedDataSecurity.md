---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230257"
---
# <span data-ttu-id="31db3-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="31db3-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="31db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31db3-102">SYNOPSIS</span></span>
<span data-ttu-id="31db3-103">Отключение advanced Data Security на сервере.</span><span class="sxs-lookup"><span data-stu-id="31db3-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="31db3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31db3-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31db3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31db3-105">DESCRIPTION</span></span>
<span data-ttu-id="31db3-106">Для отключения advanced Data Security на сервере служит cmdlet **Disable-AzSqlServerAdvancedDataSecurity.**</span><span class="sxs-lookup"><span data-stu-id="31db3-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="31db3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31db3-107">EXAMPLES</span></span>

### <span data-ttu-id="31db3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31db3-108">Example 1</span></span>
### <span data-ttu-id="31db3-109">Пример 2. Отключение расширенных служб безопасности данных на сервере</span><span class="sxs-lookup"><span data-stu-id="31db3-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="31db3-110">Пример 3. Отключение серверной расширенный безопасности данных от ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="31db3-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="31db3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31db3-111">PARAMETERS</span></span>

### <span data-ttu-id="31db3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31db3-112">-DefaultProfile</span></span>
<span data-ttu-id="31db3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31db3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31db3-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31db3-114">-InputObject</span></span>
<span data-ttu-id="31db3-115">Объект сервера, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="31db3-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31db3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31db3-116">-ResourceGroupName</span></span>
<span data-ttu-id="31db3-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31db3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="31db3-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31db3-118">-ServerName</span></span>
<span data-ttu-id="31db3-119">SQL имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="31db3-119">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31db3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31db3-120">-Confirm</span></span>
<span data-ttu-id="31db3-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31db3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31db3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31db3-122">-WhatIf</span></span>
<span data-ttu-id="31db3-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31db3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31db3-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31db3-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31db3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31db3-125">CommonParameters</span></span>
<span data-ttu-id="31db3-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31db3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31db3-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31db3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31db3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31db3-128">INPUTS</span></span>

### <span data-ttu-id="31db3-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="31db3-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="31db3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="31db3-130">System.String</span></span>

## <span data-ttu-id="31db3-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31db3-131">OUTPUTS</span></span>

### <span data-ttu-id="31db3-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="31db3-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="31db3-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31db3-133">NOTES</span></span>

## <span data-ttu-id="31db3-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31db3-134">RELATED LINKS</span></span>
