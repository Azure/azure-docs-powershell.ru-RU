---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569132"
---
# <span data-ttu-id="b41ef-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b41ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b41ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b41ef-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ef-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b41ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b41ef-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b41ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b41ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b41ef-106">Командлет **New-AzureRmWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="b41ef-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b41ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b41ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b41ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b41ef-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="b41ef-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="b41ef-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b41ef-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b41ef-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b41ef-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b41ef-111">PARAMETERS</span></span>

### <span data-ttu-id="b41ef-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b41ef-112">-AppServicePlan</span></span>
<span data-ttu-id="b41ef-113">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b41ef-113">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b41ef-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="b41ef-115">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="b41ef-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b41ef-116">-AseName</span></span>
<span data-ttu-id="b41ef-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b41ef-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41ef-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b41ef-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b41ef-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b41ef-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b41ef-121">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="b41ef-121">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b41ef-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="b41ef-123">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="b41ef-123">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b41ef-124">-Name</span></span>
<span data-ttu-id="b41ef-125">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="b41ef-125">Webapp Name</span></span>

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

### <span data-ttu-id="b41ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="b41ef-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b41ef-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="b41ef-128">-Slot</span></span>
<span data-ttu-id="b41ef-129">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="b41ef-129">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b41ef-130">-SourceWebApp</span></span>
<span data-ttu-id="b41ef-131">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="b41ef-131">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41ef-132">-DefaultProfile</span></span>
<span data-ttu-id="b41ef-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b41ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41ef-134">CommonParameters</span></span>
<span data-ttu-id="b41ef-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b41ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41ef-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41ef-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b41ef-137">INPUTS</span></span>

### <span data-ttu-id="b41ef-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="b41ef-138">Site</span></span>
<span data-ttu-id="b41ef-139">Параметр "SourceWebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b41ef-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b41ef-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b41ef-140">OUTPUTS</span></span>

## <span data-ttu-id="b41ef-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b41ef-141">NOTES</span></span>

## <span data-ttu-id="b41ef-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b41ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="b41ef-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-145">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-148">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b41ef-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b41ef-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b41ef-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b41ef-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b41ef-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
