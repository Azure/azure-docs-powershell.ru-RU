---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404508"
---
# <span data-ttu-id="d53e7-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="d53e7-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="d53e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d53e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d53e7-103">Возвращает действие для конфигурации восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="d53e7-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="d53e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d53e7-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d53e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d53e7-105">DESCRIPTION</span></span>
<span data-ttu-id="d53e7-106">Для конфигурации восстановления сервера базы данных на сервере базы данных **Get-AzSqlServerDisasterRecoveryConfigurationActivity** возвращается действие для SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="d53e7-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d53e7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d53e7-107">EXAMPLES</span></span>

## <span data-ttu-id="d53e7-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d53e7-108">PARAMETERS</span></span>

### <span data-ttu-id="d53e7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53e7-109">-DefaultProfile</span></span>
<span data-ttu-id="d53e7-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d53e7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d53e7-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d53e7-111">-OperationId</span></span>
<span data-ttu-id="d53e7-112">Определяет ИД операции.</span><span class="sxs-lookup"><span data-stu-id="d53e7-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d53e7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53e7-113">-ResourceGroupName</span></span>
<span data-ttu-id="d53e7-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d53e7-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d53e7-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d53e7-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="d53e7-116">Указывает имя конфигурации восстановления серверной системы.</span><span class="sxs-lookup"><span data-stu-id="d53e7-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="d53e7-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d53e7-117">-ServerName</span></span>
<span data-ttu-id="d53e7-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d53e7-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d53e7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d53e7-119">-Confirm</span></span>
<span data-ttu-id="d53e7-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d53e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53e7-121">-WhatIf</span></span>
<span data-ttu-id="d53e7-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d53e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53e7-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d53e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53e7-124">CommonParameters</span></span>
<span data-ttu-id="d53e7-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53e7-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d53e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53e7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d53e7-127">INPUTS</span></span>

### <span data-ttu-id="d53e7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d53e7-128">System.String</span></span>

### <span data-ttu-id="d53e7-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d53e7-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d53e7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d53e7-130">OUTPUTS</span></span>

### <span data-ttu-id="d53e7-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="d53e7-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="d53e7-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d53e7-132">NOTES</span></span>

## <span data-ttu-id="d53e7-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d53e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="d53e7-134">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d53e7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
