---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969608"
---
# <span data-ttu-id="4eeca-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4eeca-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="4eeca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eeca-102">SYNOPSIS</span></span>
<span data-ttu-id="4eeca-103">Создание в памяти объекта для расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="4eeca-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="4eeca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4eeca-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="4eeca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eeca-105">DESCRIPTION</span></span>
<span data-ttu-id="4eeca-106">Создание в памяти объекта для расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="4eeca-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="4eeca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4eeca-107">EXAMPLES</span></span>

### <span data-ttu-id="4eeca-108">Пример 1. Создание объекта расширения диагностики</span><span class="sxs-lookup"><span data-stu-id="4eeca-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="4eeca-109">Эта команда создает объект расширения диагностики, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="4eeca-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="4eeca-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="4eeca-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="4eeca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eeca-111">PARAMETERS</span></span>

### <span data-ttu-id="4eeca-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4eeca-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4eeca-113">Автоматическое обновление незначительных версий.</span><span class="sxs-lookup"><span data-stu-id="4eeca-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="4eeca-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="4eeca-114">-CloudServiceName</span></span>
<span data-ttu-id="4eeca-115">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="4eeca-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="4eeca-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="4eeca-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="4eeca-117">Определяет конфигурацию для центра диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="4eeca-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="4eeca-118">Схему можно скачать с помощью следующей команды: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="4eeca-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

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

### <span data-ttu-id="4eeca-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4eeca-119">-Name</span></span>
<span data-ttu-id="4eeca-120">Имя расширения диагностики.</span><span class="sxs-lookup"><span data-stu-id="4eeca-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="4eeca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eeca-121">-ResourceGroupName</span></span>
<span data-ttu-id="4eeca-122">Имя группы ресурсов облачной службы.</span><span class="sxs-lookup"><span data-stu-id="4eeca-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="4eeca-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="4eeca-123">-RolesAppliedTo</span></span>
<span data-ttu-id="4eeca-124">Применены роли.</span><span class="sxs-lookup"><span data-stu-id="4eeca-124">Roles applied to.</span></span>

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

### <span data-ttu-id="4eeca-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4eeca-125">-StorageAccountKey</span></span>
<span data-ttu-id="4eeca-126">Ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4eeca-126">Storage Account Key.</span></span>

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

### <span data-ttu-id="4eeca-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4eeca-127">-StorageAccountName</span></span>
<span data-ttu-id="4eeca-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4eeca-128">Name of the Storage Account.</span></span>

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

### <span data-ttu-id="4eeca-129">-Подписка</span><span class="sxs-lookup"><span data-stu-id="4eeca-129">-Subscription</span></span>
<span data-ttu-id="4eeca-130">Подписка.</span><span class="sxs-lookup"><span data-stu-id="4eeca-130">Subscription.</span></span>

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

### <span data-ttu-id="4eeca-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4eeca-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="4eeca-132">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="4eeca-132">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="4eeca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eeca-133">CommonParameters</span></span>
<span data-ttu-id="4eeca-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eeca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eeca-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eeca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eeca-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eeca-136">INPUTS</span></span>

## <span data-ttu-id="4eeca-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eeca-137">OUTPUTS</span></span>

### <span data-ttu-id="4eeca-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="4eeca-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="4eeca-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4eeca-139">NOTES</span></span>

<span data-ttu-id="4eeca-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4eeca-140">ALIASES</span></span>

## <span data-ttu-id="4eeca-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eeca-141">RELATED LINKS</span></span>

