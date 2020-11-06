---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d9763bf02054962eac955188860e97ed271d7a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561400"
---
# <span data-ttu-id="bffba-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bffba-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="bffba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bffba-102">SYNOPSIS</span></span>
<span data-ttu-id="bffba-103">Удаление политики обнаружения угроз с сервера.</span><span class="sxs-lookup"><span data-stu-id="bffba-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bffba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bffba-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bffba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bffba-105">DESCRIPTION</span></span>
<span data-ttu-id="bffba-106">Командлет Remove-AzureRmSqlServerThreatDetectionPolicy удаляет политику обнаружения угроз с сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bffba-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="bffba-107">Чтобы использовать этот командлет, укажите параметры ResourceGroupName и ServerName для идентификации сервера, с которого этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="bffba-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="bffba-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bffba-108">EXAMPLES</span></span>

### <span data-ttu-id="bffba-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="bffba-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="bffba-110">Эта команда удаляет политику обнаружения угроз с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="bffba-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="bffba-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bffba-111">PARAMETERS</span></span>

### <span data-ttu-id="bffba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffba-112">-DefaultProfile</span></span>
<span data-ttu-id="bffba-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bffba-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bffba-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bffba-114">-PassThru</span></span>
<span data-ttu-id="bffba-115">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bffba-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bffba-116">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bffba-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bffba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bffba-117">-ResourceGroupName</span></span>
<span data-ttu-id="bffba-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="bffba-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="bffba-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bffba-119">-ServerName</span></span>
<span data-ttu-id="bffba-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bffba-120">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffba-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bffba-121">-Confirm</span></span>
<span data-ttu-id="bffba-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bffba-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bffba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bffba-123">-WhatIf</span></span>
<span data-ttu-id="bffba-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bffba-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bffba-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bffba-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bffba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffba-126">CommonParameters</span></span>
<span data-ttu-id="bffba-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bffba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffba-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bffba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffba-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bffba-129">INPUTS</span></span>

###  
<span data-ttu-id="bffba-130">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bffba-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="bffba-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bffba-131">OUTPUTS</span></span>

### <span data-ttu-id="bffba-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bffba-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="bffba-133">Этот командлет возвращает объект ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="bffba-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="bffba-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bffba-134">NOTES</span></span>

## <span data-ttu-id="bffba-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bffba-135">RELATED LINKS</span></span>

[<span data-ttu-id="bffba-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bffba-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

