---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a9320219e05e61bcd77f15dd526ad45794bd45bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570387"
---
# <span data-ttu-id="348d0-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="348d0-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="348d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="348d0-102">SYNOPSIS</span></span>
<span data-ttu-id="348d0-103">Создание схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="348d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="348d0-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="348d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="348d0-105">DESCRIPTION</span></span>
<span data-ttu-id="348d0-106">Командлет **New-AzureRmIntegrationAccountSchema** создает схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="348d0-107">Этот командлет возвращает объект, представляющий схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="348d0-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя схемы и определение схемы.</span><span class="sxs-lookup"><span data-stu-id="348d0-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>

<span data-ttu-id="348d0-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="348d0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="348d0-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="348d0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="348d0-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="348d0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="348d0-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="348d0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="348d0-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="348d0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="348d0-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="348d0-114">EXAMPLES</span></span>

### <span data-ttu-id="348d0-115">Пример 1: Создание схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="348d0-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="348d0-116">Эта команда создает схему учетной записи интеграции с именем IntegrationAccountSchema1 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="348d0-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="348d0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="348d0-117">PARAMETERS</span></span>

### <span data-ttu-id="348d0-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="348d0-118">-ContentType</span></span>
<span data-ttu-id="348d0-119">Указывает тип контента для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="348d0-120">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="348d0-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="348d0-121">-Metadata</span><span class="sxs-lookup"><span data-stu-id="348d0-121">-Metadata</span></span>
<span data-ttu-id="348d0-122">Задает объект метаданных для схемы.</span><span class="sxs-lookup"><span data-stu-id="348d0-122">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="348d0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="348d0-123">-Name</span></span>
<span data-ttu-id="348d0-124">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="348d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="348d0-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="348d0-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="348d0-127">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="348d0-127">-SchemaDefinition</span></span>
<span data-ttu-id="348d0-128">Указывает объект определения для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-128">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="348d0-129">Укажите либо этот параметр, либо параметр *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="348d0-129">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="348d0-130">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="348d0-130">-SchemaFilePath</span></span>
<span data-ttu-id="348d0-131">Задает путь к файлу определения схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-131">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="348d0-132">Укажите либо этот параметр, либо параметр *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="348d0-132">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="348d0-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="348d0-133">-SchemaName</span></span>
<span data-ttu-id="348d0-134">Задает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-134">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="348d0-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="348d0-135">-SchemaType</span></span>
<span data-ttu-id="348d0-136">Указывает тип схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="348d0-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="348d0-137">Этот параметр поддерживает XML в качестве типа.</span><span class="sxs-lookup"><span data-stu-id="348d0-137">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348d0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="348d0-138">-Confirm</span></span>
<span data-ttu-id="348d0-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="348d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="348d0-140">-WhatIf</span></span>
<span data-ttu-id="348d0-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="348d0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="348d0-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="348d0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348d0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348d0-143">-DefaultProfile</span></span>
<span data-ttu-id="348d0-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="348d0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="348d0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348d0-145">CommonParameters</span></span>
<span data-ttu-id="348d0-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="348d0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348d0-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="348d0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348d0-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="348d0-148">INPUTS</span></span>

## <span data-ttu-id="348d0-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="348d0-149">OUTPUTS</span></span>

### <span data-ttu-id="348d0-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="348d0-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="348d0-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="348d0-151">NOTES</span></span>

## <span data-ttu-id="348d0-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="348d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="348d0-153">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="348d0-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="348d0-154">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="348d0-154">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="348d0-155">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="348d0-155">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


