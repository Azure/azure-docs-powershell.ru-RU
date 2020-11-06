---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559599"
---
# <span data-ttu-id="0c1bd-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c1bd-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="0c1bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1bd-103">Создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c1bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c1bd-104">SYNTAX</span></span>

### <span data-ttu-id="0c1bd-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c1bd-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c1bd-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c1bd-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c1bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="0c1bd-108">Командлет **New-AzureRmNotificationHub** создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="0c1bd-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="0c1bd-110">Концентраторы уведомлений примерно эквивалентны отдельным приложениям: каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="0c1bd-111">Командлет **New-AzureRmNotificationHub** предоставляет два способа создания нового концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="0c1bd-112">Вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="0c1bd-113">Затем вы можете скопировать значения этих свойств в новый центр с помощью параметра *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="0c1bd-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="0c1bd-114">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="0c1bd-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="0c1bd-115">При использовании в сочетании с командлетом **New-AzureRmNotificationHub** в ПРЕДЫДУЩЕМ примере JSON создается центр уведомлений под названием ContosoNotificationHub, который находится в центре обработки данных "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="0c1bd-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="0c1bd-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c1bd-116">EXAMPLES</span></span>

### <span data-ttu-id="0c1bd-117">Пример 1: создание концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="0c1bd-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="0c1bd-118">Эта команда создает концентратор уведомлений в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="0c1bd-119">Новая ступица будет назначена ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="0c1bd-120">Вам не нужно указывать имя или какие-либо другие сведения о конфигурации для концентратора; Эти данные будут взяты из входного файла, C:\Configurations\InternalHub.jsвключены.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="0c1bd-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c1bd-121">PARAMETERS</span></span>

### <span data-ttu-id="0c1bd-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0c1bd-122">-InputFile</span></span>
<span data-ttu-id="0c1bd-123">Задает путь к файлу JSON, содержащему значения конфигурации для нового концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c1bd-124">-Namespace</span></span>
<span data-ttu-id="0c1bd-125">Задает пространство имен, которому будет назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="0c1bd-126">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="0c1bd-127">Концентраторы уведомлений должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="0c1bd-128">Командлет **New-AzureRmNotificationHub** не может создать новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="0c1bd-129">-NotificationHubObj</span></span>
<span data-ttu-id="0c1bd-130">Указывает объект **NotificationHubAttributes** , содержащий сведения о конфигурации для нового концентратора.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0c1bd-131">-ResourceGroup</span></span>
<span data-ttu-id="0c1bd-132">Указывает группу ресурсов, которой будет назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="0c1bd-133">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="0c1bd-134">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-134">You must use an existing resource group.</span></span>
<span data-ttu-id="0c1bd-135">Командлет **New-AzureRmNotificationHub** не может создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="0c1bd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c1bd-136">-Confirm</span></span>
<span data-ttu-id="0c1bd-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c1bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c1bd-138">-WhatIf</span></span>
<span data-ttu-id="0c1bd-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c1bd-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c1bd-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1bd-141">-DefaultProfile</span></span>
<span data-ttu-id="0c1bd-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c1bd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1bd-143">CommonParameters</span></span>
<span data-ttu-id="0c1bd-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1bd-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1bd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1bd-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c1bd-146">INPUTS</span></span>

## <span data-ttu-id="0c1bd-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c1bd-147">OUTPUTS</span></span>

### <span data-ttu-id="0c1bd-148">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="0c1bd-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="0c1bd-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c1bd-149">NOTES</span></span>

## <span data-ttu-id="0c1bd-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c1bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c1bd-151">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c1bd-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="0c1bd-152">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c1bd-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="0c1bd-153">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c1bd-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


