---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560424"
---
# <span data-ttu-id="76419-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76419-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="76419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76419-102">SYNOPSIS</span></span>
<span data-ttu-id="76419-103">Удаление политики обнаружения угроз с сервера.</span><span class="sxs-lookup"><span data-stu-id="76419-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76419-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76419-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76419-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76419-105">DESCRIPTION</span></span>
<span data-ttu-id="76419-106">Командлет Remove-AzureRmSqlServerThreatDetectionPolicy удаляет политику обнаружения угроз с сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="76419-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="76419-107">Чтобы использовать этот командлет, укажите параметры ResourceGroupName и ServerName для идентификации сервера, с которого этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="76419-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="76419-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76419-108">EXAMPLES</span></span>

### <span data-ttu-id="76419-109">--------------------------Пример 1: Удаление политики обнаружения угроз для базы данных--------------------------</span><span class="sxs-lookup"><span data-stu-id="76419-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="76419-110">Эта команда удаляет политику обнаружения угроз с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="76419-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="76419-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76419-111">PARAMETERS</span></span>

### <span data-ttu-id="76419-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76419-112">-PassThru</span></span>
<span data-ttu-id="76419-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="76419-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76419-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="76419-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76419-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76419-115">-ResourceGroupName</span></span>
<span data-ttu-id="76419-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="76419-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="76419-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="76419-117">-ServerName</span></span>
<span data-ttu-id="76419-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="76419-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="76419-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76419-119">-Confirm</span></span>
<span data-ttu-id="76419-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76419-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76419-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76419-121">-WhatIf</span></span>
<span data-ttu-id="76419-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76419-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76419-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76419-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76419-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76419-124">-DefaultProfile</span></span>
<span data-ttu-id="76419-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76419-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76419-126">CommonParameters</span></span>
<span data-ttu-id="76419-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76419-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76419-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76419-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76419-129">INPUTS</span></span>

###  
<span data-ttu-id="76419-130">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="76419-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="76419-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76419-131">OUTPUTS</span></span>

### <span data-ttu-id="76419-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="76419-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="76419-133">Этот командлет возвращает объект ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="76419-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="76419-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="76419-134">NOTES</span></span>

## <span data-ttu-id="76419-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76419-135">RELATED LINKS</span></span>

[<span data-ttu-id="76419-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="76419-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

