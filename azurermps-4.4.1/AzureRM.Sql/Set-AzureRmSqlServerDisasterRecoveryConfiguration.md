---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735039"
---
# <span data-ttu-id="5df34-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5df34-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5df34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5df34-102">SYNOPSIS</span></span>
<span data-ttu-id="5df34-103">Изменяет конфигурацию восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="5df34-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5df34-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5df34-105">DESCRIPTION</span></span>
<span data-ttu-id="5df34-106">Командлет **Set-AzureRmSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию восстановления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5df34-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="5df34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5df34-107">EXAMPLES</span></span>

## <span data-ttu-id="5df34-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5df34-108">PARAMETERS</span></span>

### <span data-ttu-id="5df34-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5df34-109">-AllowDataLoss</span></span>
<span data-ttu-id="5df34-110">Указывает на то, что операция отработки отказа допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="5df34-110">Indicates that the failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df34-111">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="5df34-111">-Failover</span></span>
<span data-ttu-id="5df34-112">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="5df34-112">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df34-113">-ResourceGroupName</span></span>
<span data-ttu-id="5df34-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5df34-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5df34-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5df34-115">-ServerName</span></span>
<span data-ttu-id="5df34-116">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5df34-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="5df34-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5df34-117">-VirtualEndpointName</span></span>
<span data-ttu-id="5df34-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5df34-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df34-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5df34-119">-Confirm</span></span>
<span data-ttu-id="5df34-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5df34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df34-121">-WhatIf</span></span>
<span data-ttu-id="5df34-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5df34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df34-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5df34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df34-124">-DefaultProfile</span></span>
<span data-ttu-id="5df34-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5df34-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5df34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df34-126">CommonParameters</span></span>
<span data-ttu-id="5df34-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5df34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df34-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df34-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df34-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5df34-129">INPUTS</span></span>

## <span data-ttu-id="5df34-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5df34-130">OUTPUTS</span></span>

## <span data-ttu-id="5df34-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5df34-131">NOTES</span></span>

## <span data-ttu-id="5df34-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5df34-132">RELATED LINKS</span></span>

[<span data-ttu-id="5df34-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5df34-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5df34-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5df34-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5df34-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5df34-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5df34-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5df34-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
