---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 2f6df9b28db7ad86a3c779a166df34c48d779621
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570391"
---
# <span data-ttu-id="a66a9-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a66a9-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="a66a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a66a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a66a9-103">Создание карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a66a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a66a9-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a66a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a66a9-106">Командлет **New-AzureRmIntegrationAccountMap** создает карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="a66a9-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="a66a9-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя карты и определение карты.</span><span class="sxs-lookup"><span data-stu-id="a66a9-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="a66a9-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="a66a9-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="a66a9-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a66a9-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a66a9-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a66a9-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a66a9-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a66a9-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a66a9-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a66a9-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a66a9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a66a9-114">EXAMPLES</span></span>

### <span data-ttu-id="a66a9-115">Пример 1: создание карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a66a9-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="a66a9-116">Эта команда создает карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a66a9-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="a66a9-117">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="a66a9-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="a66a9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a66a9-118">PARAMETERS</span></span>

### <span data-ttu-id="a66a9-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a66a9-119">-ContentType</span></span>
<span data-ttu-id="a66a9-120">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="a66a9-121">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="a66a9-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="a66a9-122">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="a66a9-122">-MapDefinition</span></span>
<span data-ttu-id="a66a9-123">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-123">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="a66a9-124">Укажите либо этот параметр, либо параметр *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="a66a9-124">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="a66a9-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="a66a9-125">-MapFilePath</span></span>
<span data-ttu-id="a66a9-126">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-126">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="a66a9-127">Укажите либо этот параметр, либо параметр *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="a66a9-127">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="a66a9-128">-MapName</span><span class="sxs-lookup"><span data-stu-id="a66a9-128">-MapName</span></span>
<span data-ttu-id="a66a9-129">Указывает имя для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-129">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="a66a9-130">-MapType</span><span class="sxs-lookup"><span data-stu-id="a66a9-130">-MapType</span></span>
<span data-ttu-id="a66a9-131">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-131">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="a66a9-132">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="a66a9-132">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66a9-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a66a9-133">-Metadata</span></span>
<span data-ttu-id="a66a9-134">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="a66a9-134">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="a66a9-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a66a9-135">-Name</span></span>
<span data-ttu-id="a66a9-136">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a66a9-136">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="a66a9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66a9-137">-ResourceGroupName</span></span>
<span data-ttu-id="a66a9-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a66a9-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a66a9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a66a9-139">-Confirm</span></span>
<span data-ttu-id="a66a9-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a66a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66a9-141">-WhatIf</span></span>
<span data-ttu-id="a66a9-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a66a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a66a9-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a66a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66a9-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66a9-144">-DefaultProfile</span></span>
<span data-ttu-id="a66a9-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a66a9-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a66a9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66a9-146">CommonParameters</span></span>
<span data-ttu-id="a66a9-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a66a9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66a9-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66a9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66a9-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a66a9-149">INPUTS</span></span>

## <span data-ttu-id="a66a9-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a66a9-150">OUTPUTS</span></span>

### <span data-ttu-id="a66a9-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a66a9-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="a66a9-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="a66a9-152">NOTES</span></span>

## <span data-ttu-id="a66a9-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a66a9-153">RELATED LINKS</span></span>

[<span data-ttu-id="a66a9-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a66a9-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a66a9-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a66a9-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a66a9-156">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a66a9-156">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


