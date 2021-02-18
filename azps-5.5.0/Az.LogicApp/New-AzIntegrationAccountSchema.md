---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 8887cdf7da3b69d826bedd4f6de97a8cf39d4a6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237497"
---
# <span data-ttu-id="61414-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61414-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="61414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61414-102">SYNOPSIS</span></span>
<span data-ttu-id="61414-103">Создает схему интеграции учетной записи.</span><span class="sxs-lookup"><span data-stu-id="61414-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="61414-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61414-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61414-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61414-105">DESCRIPTION</span></span>
<span data-ttu-id="61414-106">Для создания схемы учетной записи создается схема учетной записи **New-AzIntegrationAccountSchema.**</span><span class="sxs-lookup"><span data-stu-id="61414-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="61414-107">Этот cmdlet возвращает объект, который представляет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="61414-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя схемы и определение схемы.</span><span class="sxs-lookup"><span data-stu-id="61414-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="61414-109">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="61414-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="61414-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="61414-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61414-111">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="61414-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61414-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="61414-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61414-113">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="61414-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61414-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61414-114">EXAMPLES</span></span>

### <span data-ttu-id="61414-115">Пример 1. Создание схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="61414-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="61414-116">Эта команда создает схему учетной записи интеграции IntegrationAccountSchema1 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61414-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="61414-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61414-117">PARAMETERS</span></span>

### <span data-ttu-id="61414-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="61414-118">-ContentType</span></span>
<span data-ttu-id="61414-119">Тип контента для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="61414-120">Этот cmdlet поддерживает приложение/xml как тип контента карты.</span><span class="sxs-lookup"><span data-stu-id="61414-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="61414-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61414-121">-DefaultProfile</span></span>
<span data-ttu-id="61414-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61414-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61414-123">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="61414-123">-Metadata</span></span>
<span data-ttu-id="61414-124">Определяет объект метаданных для схемы.</span><span class="sxs-lookup"><span data-stu-id="61414-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="61414-125">-Name</span><span class="sxs-lookup"><span data-stu-id="61414-125">-Name</span></span>
<span data-ttu-id="61414-126">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="61414-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61414-127">-ResourceGroupName</span></span>
<span data-ttu-id="61414-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61414-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61414-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="61414-129">-SchemaDefinition</span></span>
<span data-ttu-id="61414-130">Определяет объект определения для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="61414-131">Укажите этот параметр или *параметр SchemaFilePath.*</span><span class="sxs-lookup"><span data-stu-id="61414-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="61414-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="61414-132">-SchemaFilePath</span></span>
<span data-ttu-id="61414-133">Путь к файлу определения для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="61414-134">Укажите этот параметр или *параметр SchemaDefinition.*</span><span class="sxs-lookup"><span data-stu-id="61414-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="61414-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="61414-135">-SchemaName</span></span>
<span data-ttu-id="61414-136">Имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="61414-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="61414-137">-SchemaType</span></span>
<span data-ttu-id="61414-138">Тип схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="61414-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="61414-139">Этот параметр поддерживает XML в качестве типа.</span><span class="sxs-lookup"><span data-stu-id="61414-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="61414-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61414-140">-Confirm</span></span>
<span data-ttu-id="61414-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61414-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61414-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61414-142">-WhatIf</span></span>
<span data-ttu-id="61414-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61414-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61414-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61414-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61414-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61414-145">CommonParameters</span></span>
<span data-ttu-id="61414-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61414-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61414-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61414-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61414-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61414-148">INPUTS</span></span>

### <span data-ttu-id="61414-149">System.String</span><span class="sxs-lookup"><span data-stu-id="61414-149">System.String</span></span>

## <span data-ttu-id="61414-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61414-150">OUTPUTS</span></span>

### <span data-ttu-id="61414-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61414-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="61414-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61414-152">NOTES</span></span>

## <span data-ttu-id="61414-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61414-153">RELATED LINKS</span></span>

[<span data-ttu-id="61414-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61414-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="61414-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61414-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="61414-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61414-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


