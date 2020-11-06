---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 9b51a9e835962ea1715a458ace1ab02202068e30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566365"
---
# <span data-ttu-id="4d13d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4d13d-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="4d13d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d13d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d13d-103">Удаление политики обнаружения угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4d13d-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d13d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d13d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d13d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d13d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d13d-106">Командлет **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** удаляет политику обнаружения угроз из базы данных SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="4d13d-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="4d13d-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* , определяющие базу данных, из которой этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="4d13d-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="4d13d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d13d-108">EXAMPLES</span></span>

### <span data-ttu-id="4d13d-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="4d13d-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4d13d-110">Эта команда удаляет политику обнаружения угроз из базы данных с именем Database01 на сервере под названием Server01.</span><span class="sxs-lookup"><span data-stu-id="4d13d-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="4d13d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d13d-111">PARAMETERS</span></span>

### <span data-ttu-id="4d13d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d13d-112">-DatabaseName</span></span>
<span data-ttu-id="4d13d-113">Указывает имя базы данных, в которой следует удалить политику обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="4d13d-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d13d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d13d-114">-DefaultProfile</span></span>
<span data-ttu-id="4d13d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d13d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d13d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d13d-116">-PassThru</span></span>
<span data-ttu-id="4d13d-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4d13d-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d13d-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4d13d-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d13d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d13d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d13d-120">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="4d13d-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="4d13d-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4d13d-121">-ServerName</span></span>
<span data-ttu-id="4d13d-122">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="4d13d-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="4d13d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d13d-123">-Confirm</span></span>
<span data-ttu-id="4d13d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d13d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d13d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d13d-125">-WhatIf</span></span>
<span data-ttu-id="4d13d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d13d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d13d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d13d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d13d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d13d-128">CommonParameters</span></span>
<span data-ttu-id="4d13d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d13d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d13d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d13d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d13d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d13d-131">INPUTS</span></span>

### <span data-ttu-id="4d13d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4d13d-132">System.String</span></span>

## <span data-ttu-id="4d13d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d13d-133">OUTPUTS</span></span>

### <span data-ttu-id="4d13d-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4d13d-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="4d13d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d13d-135">NOTES</span></span>

## <span data-ttu-id="4d13d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d13d-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d13d-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4d13d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


