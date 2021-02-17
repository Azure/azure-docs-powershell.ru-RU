---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: 96651a495f08657a4cd9006545cfa104285ec7ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234809"
---
# <span data-ttu-id="3fc5c-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fc5c-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="3fc5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc5c-103">Создание в памяти объекта для расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="3fc5c-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="3fc5c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3fc5c-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="3fc5c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc5c-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc5c-106">Создание в памяти объекта для расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="3fc5c-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="3fc5c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3fc5c-107">EXAMPLES</span></span>

### <span data-ttu-id="3fc5c-108">Пример 1. Создание объекта расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="3fc5c-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="3fc5c-109">Эта команда создает объект расширения диагностики, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="3fc5c-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="3fc5c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fc5c-111">PARAMETERS</span></span>

### <span data-ttu-id="3fc5c-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3fc5c-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3fc5c-113">Автоматическое обновление незначительных версий.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="3fc5c-114">-CloudServiceName</span></span>
<span data-ttu-id="3fc5c-115">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="3fc5c-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="3fc5c-117">Определяет конфигурацию для службы диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="3fc5c-118">Схему можно скачать с помощью следующей команды: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="3fc5c-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3fc5c-119">-Name</span></span>
<span data-ttu-id="3fc5c-120">Имя расширения диагностики.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="3fc5c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc5c-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fc5c-122">Имя группы ресурсов облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="3fc5c-123">-RolesAppliedTo</span></span>
<span data-ttu-id="3fc5c-124">Применены роли.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3fc5c-125">-StorageAccountKey</span></span>
<span data-ttu-id="3fc5c-126">Ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3fc5c-127">-StorageAccountName</span></span>
<span data-ttu-id="3fc5c-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="3fc5c-129">-Subscription</span></span>
<span data-ttu-id="3fc5c-130">Подписка.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3fc5c-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="3fc5c-132">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc5c-133">CommonParameters</span></span>
<span data-ttu-id="3fc5c-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc5c-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fc5c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc5c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fc5c-136">INPUTS</span></span>

## <span data-ttu-id="3fc5c-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fc5c-137">OUTPUTS</span></span>

### <span data-ttu-id="3fc5c-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="3fc5c-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="3fc5c-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3fc5c-139">NOTES</span></span>

<span data-ttu-id="3fc5c-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3fc5c-140">ALIASES</span></span>

## <span data-ttu-id="3fc5c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fc5c-141">RELATED LINKS</span></span>

