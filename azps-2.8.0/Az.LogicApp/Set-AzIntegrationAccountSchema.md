---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: 99cbaa3b6b1c6fc471c98abee1953049d06f904b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720471"
---
# <span data-ttu-id="08aad-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="08aad-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="08aad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08aad-102">SYNOPSIS</span></span>
<span data-ttu-id="08aad-103">Изменение схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="08aad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08aad-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08aad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08aad-105">DESCRIPTION</span></span>
<span data-ttu-id="08aad-106">Командлет **Set-AzIntegrationAccountSchema** изменяет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="08aad-107">Этот командлет возвращает объект, представляющий схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="08aad-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя схемы.</span><span class="sxs-lookup"><span data-stu-id="08aad-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="08aad-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="08aad-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="08aad-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="08aad-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="08aad-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="08aad-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="08aad-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="08aad-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="08aad-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="08aad-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="08aad-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08aad-114">EXAMPLES</span></span>

### <span data-ttu-id="08aad-115">Пример 1: изменение схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="08aad-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="08aad-116">Эта команда изменяет схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="08aad-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="08aad-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08aad-117">PARAMETERS</span></span>

### <span data-ttu-id="08aad-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="08aad-118">-ContentType</span></span>
<span data-ttu-id="08aad-119">Указывает тип контента для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="08aad-120">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="08aad-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="08aad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08aad-121">-DefaultProfile</span></span>
<span data-ttu-id="08aad-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="08aad-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08aad-123">-Force</span><span class="sxs-lookup"><span data-stu-id="08aad-123">-Force</span></span>
<span data-ttu-id="08aad-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="08aad-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08aad-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="08aad-125">-Metadata</span></span>
<span data-ttu-id="08aad-126">Задает объект метаданных для схемы.</span><span class="sxs-lookup"><span data-stu-id="08aad-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="08aad-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08aad-127">-Name</span></span>
<span data-ttu-id="08aad-128">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="08aad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08aad-129">-ResourceGroupName</span></span>
<span data-ttu-id="08aad-130">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08aad-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08aad-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="08aad-131">-SchemaDefinition</span></span>
<span data-ttu-id="08aad-132">Указывает объект определения для схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="08aad-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="08aad-133">-SchemaFilePath</span></span>
<span data-ttu-id="08aad-134">Задает путь к файлу определения схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="08aad-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="08aad-135">-SchemaName</span></span>
<span data-ttu-id="08aad-136">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="08aad-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="08aad-137">-SchemaType</span></span>
<span data-ttu-id="08aad-138">Указывает тип схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="08aad-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="08aad-139">Этот параметр поддерживает XML в качестве типа.</span><span class="sxs-lookup"><span data-stu-id="08aad-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="08aad-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08aad-140">-Confirm</span></span>
<span data-ttu-id="08aad-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08aad-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08aad-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08aad-142">-WhatIf</span></span>
<span data-ttu-id="08aad-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08aad-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08aad-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08aad-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08aad-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08aad-145">CommonParameters</span></span>
<span data-ttu-id="08aad-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08aad-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08aad-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08aad-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08aad-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08aad-148">INPUTS</span></span>

### <span data-ttu-id="08aad-149">System. String</span><span class="sxs-lookup"><span data-stu-id="08aad-149">System.String</span></span>

## <span data-ttu-id="08aad-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08aad-150">OUTPUTS</span></span>

### <span data-ttu-id="08aad-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="08aad-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="08aad-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="08aad-152">NOTES</span></span>

## <span data-ttu-id="08aad-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08aad-153">RELATED LINKS</span></span>

[<span data-ttu-id="08aad-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="08aad-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="08aad-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="08aad-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="08aad-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="08aad-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


