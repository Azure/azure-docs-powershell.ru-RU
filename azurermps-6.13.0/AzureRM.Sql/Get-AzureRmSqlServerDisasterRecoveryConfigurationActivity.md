---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563959"
---
# <span data-ttu-id="10b51-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="10b51-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="10b51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10b51-102">SYNOPSIS</span></span>
<span data-ttu-id="10b51-103">Получает действия для конфигурации восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="10b51-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10b51-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b51-105">DESCRIPTION</span></span>
<span data-ttu-id="10b51-106">Командлет **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** получает действия для конфигурации восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="10b51-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="10b51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10b51-107">EXAMPLES</span></span>

## <span data-ttu-id="10b51-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10b51-108">PARAMETERS</span></span>

### <span data-ttu-id="10b51-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b51-109">-DefaultProfile</span></span>
<span data-ttu-id="10b51-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10b51-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b51-111">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="10b51-111">-OperationId</span></span>
<span data-ttu-id="10b51-112">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="10b51-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="10b51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b51-113">-ResourceGroupName</span></span>
<span data-ttu-id="10b51-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10b51-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="10b51-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="10b51-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="10b51-116">Указывает имя конфигурации восстановления системы сервера.</span><span class="sxs-lookup"><span data-stu-id="10b51-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="10b51-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="10b51-117">-ServerName</span></span>
<span data-ttu-id="10b51-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="10b51-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="10b51-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10b51-119">-Confirm</span></span>
<span data-ttu-id="10b51-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10b51-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b51-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b51-121">-WhatIf</span></span>
<span data-ttu-id="10b51-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10b51-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b51-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10b51-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b51-124">CommonParameters</span></span>
<span data-ttu-id="10b51-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10b51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b51-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b51-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10b51-127">INPUTS</span></span>

### <span data-ttu-id="10b51-128">System. String</span><span class="sxs-lookup"><span data-stu-id="10b51-128">System.String</span></span>

### <span data-ttu-id="10b51-129">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="10b51-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="10b51-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b51-130">OUTPUTS</span></span>

### <span data-ttu-id="10b51-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="10b51-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="10b51-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="10b51-132">NOTES</span></span>

## <span data-ttu-id="10b51-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10b51-133">RELATED LINKS</span></span>

[<span data-ttu-id="10b51-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="10b51-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
