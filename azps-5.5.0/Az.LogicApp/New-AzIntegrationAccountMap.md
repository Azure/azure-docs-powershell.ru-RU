---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237505"
---
# <span data-ttu-id="c99db-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c99db-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="c99db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99db-102">SYNOPSIS</span></span>
<span data-ttu-id="c99db-103">Создается интеграция карты учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c99db-103">Creates an integration account map.</span></span>

## <span data-ttu-id="c99db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c99db-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c99db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99db-105">DESCRIPTION</span></span>
<span data-ttu-id="c99db-106">Для создания учетной записи **New-AzIntegrationAccountMap** создается карта интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="c99db-107">Этот cmdlet возвращает объект, который представляет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="c99db-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя карты и определение карты.</span><span class="sxs-lookup"><span data-stu-id="c99db-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="c99db-109">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="c99db-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c99db-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c99db-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c99db-111">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="c99db-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c99db-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="c99db-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c99db-113">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="c99db-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c99db-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c99db-114">EXAMPLES</span></span>

### <span data-ttu-id="c99db-115">Пример 1. Создание интеграционной карты учетной записи</span><span class="sxs-lookup"><span data-stu-id="c99db-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="c99db-116">Эта команда создает карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c99db-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="c99db-117">Эта команда определяет определение карты, храняное в переменной $MapContent предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="c99db-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="c99db-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c99db-118">Example 2</span></span>

<span data-ttu-id="c99db-119">Создается интеграция карты учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c99db-119">Creates an integration account map.</span></span> <span data-ttu-id="c99db-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c99db-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="c99db-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c99db-121">PARAMETERS</span></span>

### <span data-ttu-id="c99db-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c99db-122">-ContentType</span></span>
<span data-ttu-id="c99db-123">Тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="c99db-124">Этот cmdlet поддерживает приложения и XML как тип контента карты.</span><span class="sxs-lookup"><span data-stu-id="c99db-124">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99db-125">-DefaultProfile</span></span>
<span data-ttu-id="c99db-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c99db-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c99db-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="c99db-127">-MapDefinition</span></span>
<span data-ttu-id="c99db-128">Определяет объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="c99db-129">Укажите этот параметр или *параметр MapFilePath.*</span><span class="sxs-lookup"><span data-stu-id="c99db-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="c99db-130">-MapFilePath</span></span>
<span data-ttu-id="c99db-131">Путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="c99db-132">Укажите этот параметр или *параметр MapDefinition.*</span><span class="sxs-lookup"><span data-stu-id="c99db-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="c99db-133">-MapName</span></span>
<span data-ttu-id="c99db-134">Указывает имя для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="c99db-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="c99db-135">-MapType</span></span>
<span data-ttu-id="c99db-136">Тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="c99db-137">Этот cmdlet поддерживает Xslt как тип карты.</span><span class="sxs-lookup"><span data-stu-id="c99db-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-138">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="c99db-138">-Metadata</span></span>
<span data-ttu-id="c99db-139">Определяет объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="c99db-139">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-140">-Name</span><span class="sxs-lookup"><span data-stu-id="c99db-140">-Name</span></span>
<span data-ttu-id="c99db-141">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c99db-141">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99db-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99db-142">-ResourceGroupName</span></span>
<span data-ttu-id="c99db-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c99db-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c99db-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c99db-144">-Confirm</span></span>
<span data-ttu-id="c99db-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c99db-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c99db-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c99db-146">-WhatIf</span></span>
<span data-ttu-id="c99db-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c99db-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c99db-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c99db-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c99db-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99db-149">CommonParameters</span></span>
<span data-ttu-id="c99db-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99db-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99db-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99db-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99db-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c99db-152">INPUTS</span></span>

### <span data-ttu-id="c99db-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c99db-153">System.String</span></span>

## <span data-ttu-id="c99db-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c99db-154">OUTPUTS</span></span>

### <span data-ttu-id="c99db-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c99db-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="c99db-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c99db-156">NOTES</span></span>

## <span data-ttu-id="c99db-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c99db-157">RELATED LINKS</span></span>

[<span data-ttu-id="c99db-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c99db-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="c99db-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c99db-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="c99db-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c99db-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


