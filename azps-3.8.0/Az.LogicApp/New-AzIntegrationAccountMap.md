---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 08b107ace11f7f55fee5903f16a784ba606694cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066339"
---
# <span data-ttu-id="4d9eb-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4d9eb-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="4d9eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9eb-103">Создание карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-103">Creates an integration account map.</span></span>

## <span data-ttu-id="4d9eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d9eb-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d9eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4d9eb-106">Командлет **New-AzIntegrationAccountMap** создает карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="4d9eb-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="4d9eb-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя карты и определение карты.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="4d9eb-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="4d9eb-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4d9eb-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4d9eb-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4d9eb-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4d9eb-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d9eb-114">EXAMPLES</span></span>

### <span data-ttu-id="4d9eb-115">Пример 1: создание карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="4d9eb-115">Example 1: Create an integration account map</span></span>
```
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

<span data-ttu-id="4d9eb-116">Эта команда создает карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="4d9eb-117">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="4d9eb-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d9eb-118">PARAMETERS</span></span>

### <span data-ttu-id="4d9eb-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4d9eb-119">-ContentType</span></span>
<span data-ttu-id="4d9eb-120">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="4d9eb-121">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="4d9eb-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="4d9eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9eb-122">-DefaultProfile</span></span>
<span data-ttu-id="4d9eb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d9eb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d9eb-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="4d9eb-124">-MapDefinition</span></span>
<span data-ttu-id="4d9eb-125">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="4d9eb-126">Укажите либо этот параметр, либо параметр *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="4d9eb-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="4d9eb-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="4d9eb-127">-MapFilePath</span></span>
<span data-ttu-id="4d9eb-128">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="4d9eb-129">Укажите либо этот параметр, либо параметр *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="4d9eb-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="4d9eb-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="4d9eb-130">-MapName</span></span>
<span data-ttu-id="4d9eb-131">Указывает имя для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="4d9eb-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="4d9eb-132">-MapType</span></span>
<span data-ttu-id="4d9eb-133">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="4d9eb-134">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-134">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="4d9eb-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4d9eb-135">-Metadata</span></span>
<span data-ttu-id="4d9eb-136">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-136">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="4d9eb-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d9eb-137">-Name</span></span>
<span data-ttu-id="4d9eb-138">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="4d9eb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d9eb-139">-ResourceGroupName</span></span>
<span data-ttu-id="4d9eb-140">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4d9eb-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d9eb-141">-Confirm</span></span>
<span data-ttu-id="4d9eb-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d9eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d9eb-143">-WhatIf</span></span>
<span data-ttu-id="4d9eb-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d9eb-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d9eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9eb-146">CommonParameters</span></span>
<span data-ttu-id="4d9eb-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9eb-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d9eb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9eb-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d9eb-149">INPUTS</span></span>

### <span data-ttu-id="4d9eb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4d9eb-150">System.String</span></span>

## <span data-ttu-id="4d9eb-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d9eb-151">OUTPUTS</span></span>

### <span data-ttu-id="4d9eb-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4d9eb-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="4d9eb-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d9eb-153">NOTES</span></span>

## <span data-ttu-id="4d9eb-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d9eb-154">RELATED LINKS</span></span>

[<span data-ttu-id="4d9eb-155">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4d9eb-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="4d9eb-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4d9eb-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="4d9eb-157">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4d9eb-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


