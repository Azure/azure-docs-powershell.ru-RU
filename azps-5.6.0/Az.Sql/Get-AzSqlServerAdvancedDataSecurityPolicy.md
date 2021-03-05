---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974184"
---
# <span data-ttu-id="7fa80-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="7fa80-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="7fa80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fa80-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa80-103">Получает на сервере расширенные политики безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="7fa80-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="7fa80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7fa80-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fa80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fa80-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa80-106">Для получения политики Advanced Data Security сервера извлекается cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy.**</span><span class="sxs-lookup"><span data-stu-id="7fa80-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="7fa80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7fa80-107">EXAMPLES</span></span>

### <span data-ttu-id="7fa80-108">Пример 1. Получает расширенные сведения о безопасности данных на сервере</span><span class="sxs-lookup"><span data-stu-id="7fa80-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="7fa80-109">Пример 2. Получает с сервера advanced Data Security (Расширенные сведения о безопасности) из ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="7fa80-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="7fa80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fa80-110">PARAMETERS</span></span>

### <span data-ttu-id="7fa80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa80-111">-DefaultProfile</span></span>
<span data-ttu-id="7fa80-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa80-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa80-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fa80-113">-InputObject</span></span>
<span data-ttu-id="7fa80-114">Объект сервера, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="7fa80-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="7fa80-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa80-115">-ResourceGroupName</span></span>
<span data-ttu-id="7fa80-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fa80-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fa80-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7fa80-117">-ServerName</span></span>
<span data-ttu-id="7fa80-118">SQL имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="7fa80-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="7fa80-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa80-119">CommonParameters</span></span>
<span data-ttu-id="7fa80-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa80-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa80-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fa80-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa80-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fa80-122">INPUTS</span></span>

### <span data-ttu-id="7fa80-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7fa80-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7fa80-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7fa80-124">System.String</span></span>

## <span data-ttu-id="7fa80-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7fa80-125">OUTPUTS</span></span>

### <span data-ttu-id="7fa80-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7fa80-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="7fa80-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7fa80-127">NOTES</span></span>

## <span data-ttu-id="7fa80-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fa80-128">RELATED LINKS</span></span>
