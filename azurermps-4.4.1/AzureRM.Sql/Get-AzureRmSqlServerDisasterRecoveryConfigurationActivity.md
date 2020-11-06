---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567498"
---
# <span data-ttu-id="f8913-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="f8913-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="f8913-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8913-102">SYNOPSIS</span></span>
<span data-ttu-id="f8913-103">Получает действия для конфигурации восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="f8913-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8913-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8913-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8913-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8913-105">DESCRIPTION</span></span>
<span data-ttu-id="f8913-106">Командлет **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** получает действия для конфигурации восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f8913-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f8913-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8913-107">EXAMPLES</span></span>

## <span data-ttu-id="f8913-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8913-108">PARAMETERS</span></span>

### <span data-ttu-id="f8913-109">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="f8913-109">-OperationId</span></span>
<span data-ttu-id="f8913-110">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="f8913-110">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="f8913-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8913-111">-ResourceGroupName</span></span>
<span data-ttu-id="f8913-112">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8913-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f8913-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f8913-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="f8913-114">Указывает имя конфигурации восстановления системы сервера.</span><span class="sxs-lookup"><span data-stu-id="f8913-114">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="f8913-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f8913-115">-ServerName</span></span>
<span data-ttu-id="f8913-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f8913-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f8913-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8913-117">-Confirm</span></span>
<span data-ttu-id="f8913-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8913-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8913-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8913-119">-WhatIf</span></span>
<span data-ttu-id="f8913-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8913-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8913-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8913-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8913-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8913-122">-DefaultProfile</span></span>
<span data-ttu-id="f8913-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8913-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8913-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8913-124">CommonParameters</span></span>
<span data-ttu-id="f8913-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8913-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8913-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8913-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8913-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8913-127">INPUTS</span></span>

## <span data-ttu-id="f8913-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8913-128">OUTPUTS</span></span>

## <span data-ttu-id="f8913-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8913-129">NOTES</span></span>

## <span data-ttu-id="f8913-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8913-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8913-131">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f8913-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
