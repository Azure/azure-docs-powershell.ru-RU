---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394327"
---
# <span data-ttu-id="bfa12-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="bfa12-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="bfa12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa12-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa12-103">Удаляет дополнительные параметры защиты от угроз с сервера.</span><span class="sxs-lookup"><span data-stu-id="bfa12-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="bfa12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bfa12-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfa12-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa12-106">Этот Clear-AzSqlServerAdvancedThreatProtectionSetting удаляет дополнительные параметры защиты от угроз с SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa12-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="bfa12-107">Чтобы использовать этот cmdlet, укажите параметры ResourceGroupName и ServerName, чтобы определить сервер, с которого этот cmdlet удаляет параметры.</span><span class="sxs-lookup"><span data-stu-id="bfa12-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="bfa12-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bfa12-108">EXAMPLES</span></span>

### <span data-ttu-id="bfa12-109">Пример 1. Удаление дополнительных параметров защиты от угроз в базе данных</span><span class="sxs-lookup"><span data-stu-id="bfa12-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="bfa12-110">Эта команда удаляет дополнительные параметры защиты от угроз с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="bfa12-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="bfa12-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfa12-111">PARAMETERS</span></span>

### <span data-ttu-id="bfa12-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa12-112">-DefaultProfile</span></span>
<span data-ttu-id="bfa12-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfa12-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfa12-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfa12-114">-PassThru</span></span>
<span data-ttu-id="bfa12-115">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bfa12-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bfa12-116">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bfa12-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bfa12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa12-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfa12-118">Имя группы ресурсов, назначенной серверу.</span><span class="sxs-lookup"><span data-stu-id="bfa12-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="bfa12-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bfa12-119">-ServerName</span></span>
<span data-ttu-id="bfa12-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bfa12-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="bfa12-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa12-121">-Confirm</span></span>
<span data-ttu-id="bfa12-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bfa12-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa12-123">-WhatIf</span></span>
<span data-ttu-id="bfa12-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa12-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa12-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bfa12-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa12-126">CommonParameters</span></span>
<span data-ttu-id="bfa12-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa12-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfa12-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa12-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa12-129">INPUTS</span></span>

### <span data-ttu-id="bfa12-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bfa12-130">System.String</span></span>

## <span data-ttu-id="bfa12-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa12-131">OUTPUTS</span></span>

### <span data-ttu-id="bfa12-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="bfa12-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="bfa12-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bfa12-133">NOTES</span></span>

## <span data-ttu-id="bfa12-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfa12-134">RELATED LINKS</span></span>

[<span data-ttu-id="bfa12-135">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="bfa12-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

