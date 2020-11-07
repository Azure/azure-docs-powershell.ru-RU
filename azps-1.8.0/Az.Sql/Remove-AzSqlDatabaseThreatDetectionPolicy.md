---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: b0ca96910d763cfcf40530ad99872e1e0d50ca31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728851"
---
# <span data-ttu-id="9cfcf-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9cfcf-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="9cfcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfcf-103">Удаление политики обнаружения угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-103">Removes the threat detection policy from a database.</span></span>

## <span data-ttu-id="9cfcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cfcf-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cfcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cfcf-105">DESCRIPTION</span></span>
<span data-ttu-id="9cfcf-106">Командлет **Remove-AzSqlDatabaseThreatDetectionPolicy** удаляет политику обнаружения угроз из базы данных SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-106">The **Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="9cfcf-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* , определяющие базу данных, из которой этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="9cfcf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cfcf-108">EXAMPLES</span></span>

### <span data-ttu-id="9cfcf-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="9cfcf-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="9cfcf-110">Эта команда удаляет политику обнаружения угроз из базы данных с именем Database01 на сервере под названием Server01.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9cfcf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cfcf-111">PARAMETERS</span></span>

### <span data-ttu-id="9cfcf-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9cfcf-112">-DatabaseName</span></span>
<span data-ttu-id="9cfcf-113">Указывает имя базы данных, в которой следует удалить политику обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="9cfcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfcf-114">-DefaultProfile</span></span>
<span data-ttu-id="9cfcf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9cfcf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cfcf-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cfcf-116">-PassThru</span></span>
<span data-ttu-id="9cfcf-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cfcf-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cfcf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfcf-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cfcf-120">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="9cfcf-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9cfcf-121">-ServerName</span></span>
<span data-ttu-id="9cfcf-122">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="9cfcf-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cfcf-123">-Confirm</span></span>
<span data-ttu-id="9cfcf-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cfcf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cfcf-125">-WhatIf</span></span>
<span data-ttu-id="9cfcf-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cfcf-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cfcf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfcf-128">CommonParameters</span></span>
<span data-ttu-id="9cfcf-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfcf-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cfcf-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfcf-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cfcf-131">INPUTS</span></span>

### <span data-ttu-id="9cfcf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9cfcf-132">System.String</span></span>

## <span data-ttu-id="9cfcf-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cfcf-133">OUTPUTS</span></span>

### <span data-ttu-id="9cfcf-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9cfcf-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="9cfcf-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cfcf-135">NOTES</span></span>

## <span data-ttu-id="9cfcf-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cfcf-136">RELATED LINKS</span></span>

[<span data-ttu-id="9cfcf-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9cfcf-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


