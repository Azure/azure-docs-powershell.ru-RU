---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243938"
---
# <span data-ttu-id="cb9a7-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="cb9a7-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="cb9a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9a7-103">Отключение расширенной защиты данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="cb9a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb9a7-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb9a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9a7-106">Командлет **Disable-AzSqlServerAdvancedDataSecurity** отключает на сервере расширенную защиту данных.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="cb9a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb9a7-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9a7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb9a7-108">Example 1</span></span>
### <span data-ttu-id="cb9a7-109">Пример 2: отключение расширенной защиты данных сервера</span><span class="sxs-lookup"><span data-stu-id="cb9a7-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="cb9a7-110">Пример 3: отключение расширенной защиты данных сервера от ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="cb9a7-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="cb9a7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb9a7-111">PARAMETERS</span></span>

### <span data-ttu-id="cb9a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9a7-112">-DefaultProfile</span></span>
<span data-ttu-id="cb9a7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9a7-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb9a7-114">-InputObject</span></span>
<span data-ttu-id="cb9a7-115">Объект сервера для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="cb9a7-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="cb9a7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9a7-116">-ResourceGroupName</span></span>
<span data-ttu-id="cb9a7-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb9a7-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="cb9a7-118">-ServerName</span></span>
<span data-ttu-id="cb9a7-119">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="cb9a7-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb9a7-120">-Confirm</span></span>
<span data-ttu-id="cb9a7-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9a7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9a7-122">-WhatIf</span></span>
<span data-ttu-id="cb9a7-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9a7-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9a7-125">CommonParameters</span></span>
<span data-ttu-id="cb9a7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9a7-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb9a7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9a7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb9a7-128">INPUTS</span></span>

### <span data-ttu-id="cb9a7-129">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cb9a7-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cb9a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cb9a7-130">System.String</span></span>

## <span data-ttu-id="cb9a7-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb9a7-131">OUTPUTS</span></span>

### <span data-ttu-id="cb9a7-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb9a7-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="cb9a7-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb9a7-133">NOTES</span></span>

## <span data-ttu-id="cb9a7-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb9a7-134">RELATED LINKS</span></span>
