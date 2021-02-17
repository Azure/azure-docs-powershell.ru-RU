---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232617"
---
# <span data-ttu-id="02f27-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="02f27-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="02f27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f27-102">SYNOPSIS</span></span>
<span data-ttu-id="02f27-103">Получает действия для конфигурации восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="02f27-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="02f27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02f27-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f27-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02f27-105">DESCRIPTION</span></span>
<span data-ttu-id="02f27-106">Для конфигурации восстановления сервера базы данных на сервере базы данных **get-AzSqlServerDisasterRecoveryConfigurationActivity** возвращается действие для SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="02f27-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="02f27-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02f27-107">EXAMPLES</span></span>

## <span data-ttu-id="02f27-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02f27-108">PARAMETERS</span></span>

### <span data-ttu-id="02f27-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f27-109">-DefaultProfile</span></span>
<span data-ttu-id="02f27-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="02f27-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02f27-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="02f27-111">-OperationId</span></span>
<span data-ttu-id="02f27-112">Определяет ИД операции.</span><span class="sxs-lookup"><span data-stu-id="02f27-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="02f27-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f27-113">-ResourceGroupName</span></span>
<span data-ttu-id="02f27-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02f27-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="02f27-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="02f27-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="02f27-116">Указывает имя конфигурации восстановления серверной системы.</span><span class="sxs-lookup"><span data-stu-id="02f27-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="02f27-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02f27-117">-ServerName</span></span>
<span data-ttu-id="02f27-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="02f27-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="02f27-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02f27-119">-Confirm</span></span>
<span data-ttu-id="02f27-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f27-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f27-121">-WhatIf</span></span>
<span data-ttu-id="02f27-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f27-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02f27-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f27-124">CommonParameters</span></span>
<span data-ttu-id="02f27-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f27-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02f27-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f27-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02f27-127">INPUTS</span></span>

### <span data-ttu-id="02f27-128">System.String</span><span class="sxs-lookup"><span data-stu-id="02f27-128">System.String</span></span>

### <span data-ttu-id="02f27-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="02f27-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="02f27-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02f27-130">OUTPUTS</span></span>

### <span data-ttu-id="02f27-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="02f27-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="02f27-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02f27-132">NOTES</span></span>

## <span data-ttu-id="02f27-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02f27-133">RELATED LINKS</span></span>

[<span data-ttu-id="02f27-134">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="02f27-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
