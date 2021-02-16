---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: f71f7e37e4864de10c5387d63c101cd66ed9fd34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412628"
---
# <span data-ttu-id="8f2d5-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8f2d5-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="8f2d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2d5-103">Импортирует указанный файл параметров хранилища ASR, чтобы настроить контекст хранилища (контекст сеанса PowerShell) для последующих операций asR в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="8f2d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f2d5-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2d5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2d5-106">Для **импорта-AzRecoveryServicesAsrVaultSettingsFile** импортируется файл параметров хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="8f2d5-107">Файл параметров хранилища используется для настройки контекста хранилища для последующих операций восстановления сайта Azure в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="8f2d5-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f2d5-108">EXAMPLES</span></span>

### <span data-ttu-id="8f2d5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f2d5-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="8f2d5-110">Импорт указанного файла параметров хранилища служб восстановления и возврат параметров импортируемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="8f2d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-111">PARAMETERS</span></span>

### <span data-ttu-id="8f2d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2d5-112">-DefaultProfile</span></span>
<span data-ttu-id="8f2d5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8f2d5-114">-Path</span><span class="sxs-lookup"><span data-stu-id="8f2d5-114">-Path</span></span>
<span data-ttu-id="8f2d5-115">Путь к папке в файле параметров хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="8f2d5-116">Этот файл можно скачать с портала хранилища служб восстановления и сохранить локально.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="8f2d5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f2d5-117">-Confirm</span></span>
<span data-ttu-id="8f2d5-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2d5-119">-WhatIf</span></span>
<span data-ttu-id="8f2d5-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f2d5-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2d5-122">CommonParameters</span></span>
<span data-ttu-id="8f2d5-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2d5-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2d5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-125">INPUTS</span></span>

### <span data-ttu-id="8f2d5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2d5-126">System.String</span></span>

## <span data-ttu-id="8f2d5-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-127">OUTPUTS</span></span>

### <span data-ttu-id="8f2d5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8f2d5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="8f2d5-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f2d5-129">NOTES</span></span>

## <span data-ttu-id="8f2d5-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f2d5-130">RELATED LINKS</span></span>

