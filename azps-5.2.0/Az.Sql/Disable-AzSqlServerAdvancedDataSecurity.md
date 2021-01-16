---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394279"
---
# <span data-ttu-id="4af55-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="4af55-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="4af55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af55-102">SYNOPSIS</span></span>
<span data-ttu-id="4af55-103">Отключение advanced Data Security на сервере.</span><span class="sxs-lookup"><span data-stu-id="4af55-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="4af55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4af55-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4af55-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af55-105">DESCRIPTION</span></span>
<span data-ttu-id="4af55-106">Для отключения advanced Data Security на сервере служит cmdlet **Disable-AzSqlServerAdvancedDataSecurity.**</span><span class="sxs-lookup"><span data-stu-id="4af55-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="4af55-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4af55-107">EXAMPLES</span></span>

### <span data-ttu-id="4af55-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4af55-108">Example 1</span></span>
### <span data-ttu-id="4af55-109">Пример 2. Отключение расширенных служб безопасности данных на сервере</span><span class="sxs-lookup"><span data-stu-id="4af55-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="4af55-110">Пример 3. Отключение серверной расширенный безопасности данных от ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="4af55-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="4af55-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4af55-111">PARAMETERS</span></span>

### <span data-ttu-id="4af55-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af55-112">-DefaultProfile</span></span>
<span data-ttu-id="4af55-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4af55-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af55-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4af55-114">-InputObject</span></span>
<span data-ttu-id="4af55-115">Объект сервера, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="4af55-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="4af55-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af55-116">-ResourceGroupName</span></span>
<span data-ttu-id="4af55-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4af55-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="4af55-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4af55-118">-ServerName</span></span>
<span data-ttu-id="4af55-119">SQL имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="4af55-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="4af55-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4af55-120">-Confirm</span></span>
<span data-ttu-id="4af55-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4af55-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4af55-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af55-122">-WhatIf</span></span>
<span data-ttu-id="4af55-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af55-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4af55-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4af55-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4af55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af55-125">CommonParameters</span></span>
<span data-ttu-id="4af55-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af55-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4af55-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af55-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4af55-128">INPUTS</span></span>

### <span data-ttu-id="4af55-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="4af55-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4af55-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4af55-130">System.String</span></span>

## <span data-ttu-id="4af55-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4af55-131">OUTPUTS</span></span>

### <span data-ttu-id="4af55-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4af55-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="4af55-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4af55-133">NOTES</span></span>

## <span data-ttu-id="4af55-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af55-134">RELATED LINKS</span></span>
