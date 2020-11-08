---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243917"
---
# <span data-ttu-id="fd8b5-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="fd8b5-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="fd8b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8b5-103">Получает расширенную политику безопасности данных сервера.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="fd8b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd8b5-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd8b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd8b5-106">Командлет **Get-AzSqlServerAdvancedDataSecurityPolicy** получает дополнительные политики безопасности данных сервера.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="fd8b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd8b5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd8b5-108">Пример 1: получение расширенной защиты данных сервера</span><span class="sxs-lookup"><span data-stu-id="fd8b5-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="fd8b5-109">Пример 2: получение расширенной защиты данных сервера от ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="fd8b5-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="fd8b5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd8b5-110">PARAMETERS</span></span>

### <span data-ttu-id="fd8b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b5-111">-DefaultProfile</span></span>
<span data-ttu-id="fd8b5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8b5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd8b5-113">-InputObject</span></span>
<span data-ttu-id="fd8b5-114">Объект сервера для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="fd8b5-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="fd8b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd8b5-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd8b5-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fd8b5-117">-ServerName</span></span>
<span data-ttu-id="fd8b5-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="fd8b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8b5-119">CommonParameters</span></span>
<span data-ttu-id="fd8b5-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd8b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8b5-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd8b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8b5-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd8b5-122">INPUTS</span></span>

### <span data-ttu-id="fd8b5-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fd8b5-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fd8b5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fd8b5-124">System.String</span></span>

## <span data-ttu-id="fd8b5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8b5-125">OUTPUTS</span></span>

### <span data-ttu-id="fd8b5-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fd8b5-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="fd8b5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd8b5-127">NOTES</span></span>

## <span data-ttu-id="fd8b5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd8b5-128">RELATED LINKS</span></span>
