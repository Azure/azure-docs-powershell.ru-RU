---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967587"
---
# <span data-ttu-id="33c49-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="33c49-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="33c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33c49-102">SYNOPSIS</span></span>
<span data-ttu-id="33c49-103">Отключение advanced Data Security на сервере.</span><span class="sxs-lookup"><span data-stu-id="33c49-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="33c49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33c49-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33c49-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33c49-105">DESCRIPTION</span></span>
<span data-ttu-id="33c49-106">Для отключения advanced Data Security на сервере служит cmdlet **Disable-AzSqlServerAdvancedDataSecurity.**</span><span class="sxs-lookup"><span data-stu-id="33c49-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="33c49-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33c49-107">EXAMPLES</span></span>

### <span data-ttu-id="33c49-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33c49-108">Example 1</span></span>
### <span data-ttu-id="33c49-109">Пример 2. Отключение расширенных служб безопасности данных на сервере</span><span class="sxs-lookup"><span data-stu-id="33c49-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="33c49-110">Пример 3. Отключение серверной расширенный безопасности данных от ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="33c49-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="33c49-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33c49-111">PARAMETERS</span></span>

### <span data-ttu-id="33c49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c49-112">-DefaultProfile</span></span>
<span data-ttu-id="33c49-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33c49-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c49-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33c49-114">-InputObject</span></span>
<span data-ttu-id="33c49-115">Объект сервера, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="33c49-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="33c49-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c49-116">-ResourceGroupName</span></span>
<span data-ttu-id="33c49-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33c49-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="33c49-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33c49-118">-ServerName</span></span>
<span data-ttu-id="33c49-119">SQL имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="33c49-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="33c49-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33c49-120">-Confirm</span></span>
<span data-ttu-id="33c49-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="33c49-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c49-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c49-122">-WhatIf</span></span>
<span data-ttu-id="33c49-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c49-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33c49-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="33c49-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c49-125">CommonParameters</span></span>
<span data-ttu-id="33c49-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c49-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c49-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c49-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33c49-128">INPUTS</span></span>

### <span data-ttu-id="33c49-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="33c49-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="33c49-130">System.String</span><span class="sxs-lookup"><span data-stu-id="33c49-130">System.String</span></span>

## <span data-ttu-id="33c49-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33c49-131">OUTPUTS</span></span>

### <span data-ttu-id="33c49-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="33c49-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="33c49-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33c49-133">NOTES</span></span>

## <span data-ttu-id="33c49-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33c49-134">RELATED LINKS</span></span>
