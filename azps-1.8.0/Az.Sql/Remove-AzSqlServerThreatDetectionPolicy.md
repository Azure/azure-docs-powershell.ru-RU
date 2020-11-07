---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728824"
---
# <span data-ttu-id="b29f3-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b29f3-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="b29f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b29f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b29f3-103">Удаление политики обнаружения угроз с сервера.</span><span class="sxs-lookup"><span data-stu-id="b29f3-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="b29f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b29f3-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b29f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b29f3-105">DESCRIPTION</span></span>
<span data-ttu-id="b29f3-106">Командлет Remove-AzSqlServerThreatDetectionPolicy удаляет политику обнаружения угроз с сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b29f3-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="b29f3-107">Чтобы использовать этот командлет, укажите параметры ResourceGroupName и ServerName для идентификации сервера, с которого этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="b29f3-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="b29f3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b29f3-108">EXAMPLES</span></span>

### <span data-ttu-id="b29f3-109">Пример 1: Удаление политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="b29f3-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b29f3-110">Эта команда удаляет политику обнаружения угроз с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="b29f3-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="b29f3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b29f3-111">PARAMETERS</span></span>

### <span data-ttu-id="b29f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29f3-112">-DefaultProfile</span></span>
<span data-ttu-id="b29f3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b29f3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b29f3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b29f3-114">-PassThru</span></span>
<span data-ttu-id="b29f3-115">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b29f3-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b29f3-116">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b29f3-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b29f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="b29f3-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="b29f3-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b29f3-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b29f3-119">-ServerName</span></span>
<span data-ttu-id="b29f3-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b29f3-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b29f3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b29f3-121">-Confirm</span></span>
<span data-ttu-id="b29f3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b29f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b29f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b29f3-123">-WhatIf</span></span>
<span data-ttu-id="b29f3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b29f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b29f3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b29f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b29f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29f3-126">CommonParameters</span></span>
<span data-ttu-id="b29f3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b29f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29f3-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b29f3-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29f3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b29f3-129">INPUTS</span></span>

### <span data-ttu-id="b29f3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b29f3-130">System.String</span></span>

## <span data-ttu-id="b29f3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b29f3-131">OUTPUTS</span></span>

### <span data-ttu-id="b29f3-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b29f3-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="b29f3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b29f3-133">NOTES</span></span>

## <span data-ttu-id="b29f3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b29f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="b29f3-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b29f3-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

