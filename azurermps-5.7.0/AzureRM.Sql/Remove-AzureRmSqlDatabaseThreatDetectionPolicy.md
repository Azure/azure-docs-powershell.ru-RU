---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 8e0c13565641a6033a22545d95af28df1c14a772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561412"
---
# <span data-ttu-id="9e262-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e262-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="9e262-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e262-102">SYNOPSIS</span></span>
<span data-ttu-id="9e262-103">Удаление политики обнаружения угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e262-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e262-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e262-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e262-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e262-105">DESCRIPTION</span></span>
<span data-ttu-id="9e262-106">Командлет **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** удаляет политику обнаружения угроз из базы данных SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="9e262-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="9e262-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* , определяющие базу данных, из которой этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="9e262-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="9e262-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e262-108">EXAMPLES</span></span>

### <span data-ttu-id="9e262-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="9e262-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="9e262-110">Эта команда удаляет политику обнаружения угроз из базы данных с именем Database01 на сервере под названием Server01.</span><span class="sxs-lookup"><span data-stu-id="9e262-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9e262-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e262-111">PARAMETERS</span></span>

### <span data-ttu-id="9e262-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9e262-112">-DatabaseName</span></span>
<span data-ttu-id="9e262-113">Указывает имя базы данных, в которой следует удалить политику обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="9e262-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e262-114">-DefaultProfile</span></span>
<span data-ttu-id="9e262-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e262-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e262-116">-PassThru</span></span>
<span data-ttu-id="9e262-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9e262-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e262-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9e262-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e262-119">-ResourceGroupName</span></span>
<span data-ttu-id="9e262-120">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="9e262-120">Specifies the name of the resource group the server belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9e262-121">-ServerName</span></span>
<span data-ttu-id="9e262-122">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="9e262-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e262-123">-Confirm</span></span>
<span data-ttu-id="9e262-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e262-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e262-125">-WhatIf</span></span>
<span data-ttu-id="9e262-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e262-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e262-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e262-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e262-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e262-128">CommonParameters</span></span>
<span data-ttu-id="9e262-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e262-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e262-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e262-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e262-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e262-131">INPUTS</span></span>

###  
<span data-ttu-id="9e262-132">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e262-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="9e262-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e262-133">OUTPUTS</span></span>

### <span data-ttu-id="9e262-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9e262-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="9e262-135">Этот командлет возвращает объект **DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="9e262-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="9e262-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e262-136">NOTES</span></span>

## <span data-ttu-id="9e262-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e262-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e262-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9e262-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


