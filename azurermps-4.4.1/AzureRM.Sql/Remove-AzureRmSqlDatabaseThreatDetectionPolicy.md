---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 723e765435aae739e6d58320276f7df8ac06ba66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570051"
---
# <span data-ttu-id="01dfa-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="01dfa-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="01dfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="01dfa-103">Удаление политики обнаружения угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="01dfa-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01dfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01dfa-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01dfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="01dfa-106">Командлет **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** удаляет политику обнаружения угроз из базы данных SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="01dfa-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="01dfa-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* , определяющие базу данных, из которой этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="01dfa-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="01dfa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01dfa-108">EXAMPLES</span></span>

### <span data-ttu-id="01dfa-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="01dfa-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="01dfa-110">Эта команда удаляет политику обнаружения угроз из базы данных с именем Database01 на сервере под названием Server01.</span><span class="sxs-lookup"><span data-stu-id="01dfa-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="01dfa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01dfa-111">PARAMETERS</span></span>

### <span data-ttu-id="01dfa-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01dfa-112">-DatabaseName</span></span>
<span data-ttu-id="01dfa-113">Указывает имя базы данных, в которой следует удалить политику обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="01dfa-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="01dfa-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01dfa-114">-PassThru</span></span>
<span data-ttu-id="01dfa-115">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="01dfa-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01dfa-116">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="01dfa-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01dfa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01dfa-117">-ResourceGroupName</span></span>
<span data-ttu-id="01dfa-118">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="01dfa-118">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="01dfa-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="01dfa-119">-ServerName</span></span>
<span data-ttu-id="01dfa-120">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="01dfa-120">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="01dfa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01dfa-121">-Confirm</span></span>
<span data-ttu-id="01dfa-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01dfa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dfa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dfa-123">-WhatIf</span></span>
<span data-ttu-id="01dfa-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01dfa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01dfa-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01dfa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dfa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dfa-126">-DefaultProfile</span></span>
<span data-ttu-id="01dfa-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01dfa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01dfa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dfa-128">CommonParameters</span></span>
<span data-ttu-id="01dfa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01dfa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dfa-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01dfa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dfa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01dfa-131">INPUTS</span></span>

###  
<span data-ttu-id="01dfa-132">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="01dfa-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="01dfa-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01dfa-133">OUTPUTS</span></span>

### <span data-ttu-id="01dfa-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="01dfa-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="01dfa-135">Этот командлет возвращает объект **DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="01dfa-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="01dfa-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="01dfa-136">NOTES</span></span>

## <span data-ttu-id="01dfa-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01dfa-137">RELATED LINKS</span></span>

[<span data-ttu-id="01dfa-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="01dfa-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


