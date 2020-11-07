---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728325"
---
# <span data-ttu-id="09410-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="09410-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09410-102">SYNOPSIS</span></span>
<span data-ttu-id="09410-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="09410-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="09410-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09410-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09410-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09410-105">DESCRIPTION</span></span>
<span data-ttu-id="09410-106">Командлет **New-AzWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="09410-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="09410-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09410-107">EXAMPLES</span></span>

### <span data-ttu-id="09410-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09410-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="09410-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="09410-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="09410-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="09410-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="09410-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09410-111">PARAMETERS</span></span>

### <span data-ttu-id="09410-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09410-112">-AppServicePlan</span></span>
<span data-ttu-id="09410-113">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="09410-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="09410-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="09410-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="09410-115">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="09410-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="09410-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="09410-116">-AseName</span></span>
<span data-ttu-id="09410-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="09410-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="09410-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09410-118">-AseResourceGroupName</span></span>
<span data-ttu-id="09410-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="09410-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="09410-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09410-120">-AsJob</span></span>
<span data-ttu-id="09410-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="09410-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09410-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="09410-122">-ContainerImageName</span></span>
<span data-ttu-id="09410-123">Имя и дополнительный тег в контейнере, например (изображение: тег)</span><span class="sxs-lookup"><span data-stu-id="09410-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="09410-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="09410-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="09410-125">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="09410-125">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09410-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="09410-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="09410-127">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="09410-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="09410-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="09410-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="09410-129">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="09410-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="09410-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09410-130">-DefaultProfile</span></span>
<span data-ttu-id="09410-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09410-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09410-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="09410-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="09410-133">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="09410-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="09410-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="09410-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="09410-135">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="09410-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="09410-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="09410-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="09410-137">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="09410-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="09410-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09410-138">-Name</span></span>
<span data-ttu-id="09410-139">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="09410-139">Webapp Name</span></span>

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

### <span data-ttu-id="09410-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09410-140">-ResourceGroupName</span></span>
<span data-ttu-id="09410-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="09410-141">Resource Group Name</span></span>

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

### <span data-ttu-id="09410-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="09410-142">-Slot</span></span>
<span data-ttu-id="09410-143">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="09410-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="09410-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="09410-144">-SourceWebApp</span></span>
<span data-ttu-id="09410-145">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="09410-145">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09410-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09410-146">CommonParameters</span></span>
<span data-ttu-id="09410-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09410-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09410-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09410-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09410-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09410-149">INPUTS</span></span>

### <span data-ttu-id="09410-150">System. String</span><span class="sxs-lookup"><span data-stu-id="09410-150">System.String</span></span>

### <span data-ttu-id="09410-151">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="09410-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="09410-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09410-152">OUTPUTS</span></span>

### <span data-ttu-id="09410-153">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="09410-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="09410-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="09410-154">NOTES</span></span>

## <span data-ttu-id="09410-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09410-155">RELATED LINKS</span></span>

[<span data-ttu-id="09410-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="09410-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="09410-158">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="09410-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="09410-160">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="09410-161">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09410-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="09410-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="09410-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="09410-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="09410-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
