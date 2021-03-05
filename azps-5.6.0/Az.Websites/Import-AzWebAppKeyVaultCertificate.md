---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007416"
---
# <span data-ttu-id="84a22-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84a22-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="84a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a22-102">SYNOPSIS</span></span>
<span data-ttu-id="84a22-103">Импорт SSL-сертификата в веб-приложение из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="84a22-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="84a22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84a22-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84a22-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84a22-105">DESCRIPTION</span></span>
<span data-ttu-id="84a22-106">При **импорте-AzWebAppKeyVaultCertificate SSL-сертификат** импортируется в веб-приложение из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="84a22-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="84a22-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84a22-107">EXAMPLES</span></span>

### <span data-ttu-id="84a22-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84a22-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="84a22-109">Эта команда импортирует SSL-сертификат в веб-приложение из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="84a22-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="84a22-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="84a22-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="84a22-111">Эта команда импортирует SSL-сертификат в веб-приложение из хранилища ключей с помощью ид ресурса (обычно если хранилище ключей находится в другой подписке).</span><span class="sxs-lookup"><span data-stu-id="84a22-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="84a22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a22-112">PARAMETERS</span></span>

### <span data-ttu-id="84a22-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="84a22-113">-CertName</span></span>
<span data-ttu-id="84a22-114">KeyVaultCertName сертификата, созданного в keyvault</span><span class="sxs-lookup"><span data-stu-id="84a22-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a22-115">-DefaultProfile</span></span>
<span data-ttu-id="84a22-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84a22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a22-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="84a22-117">-KeyVaultName</span></span>
<span data-ttu-id="84a22-118">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="84a22-118">The name of the keyvault.</span></span>

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

### <span data-ttu-id="84a22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a22-119">-ResourceGroupName</span></span>
<span data-ttu-id="84a22-120">Имя группы ресурсов веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="84a22-120">The name of the webapp resource group.</span></span>

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

### <span data-ttu-id="84a22-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="84a22-121">-Slot</span></span>
<span data-ttu-id="84a22-122">Имя слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="84a22-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="84a22-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="84a22-123">-WebAppName</span></span>
<span data-ttu-id="84a22-124">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="84a22-124">The name of the webapp.</span></span>

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

### <span data-ttu-id="84a22-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84a22-125">-Confirm</span></span>
<span data-ttu-id="84a22-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="84a22-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a22-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a22-127">-WhatIf</span></span>
<span data-ttu-id="84a22-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a22-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a22-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="84a22-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a22-130">CommonParameters</span></span>
<span data-ttu-id="84a22-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a22-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a22-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a22-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84a22-133">INPUTS</span></span>

### <span data-ttu-id="84a22-134">Нет</span><span class="sxs-lookup"><span data-stu-id="84a22-134">None</span></span>

## <span data-ttu-id="84a22-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84a22-135">OUTPUTS</span></span>

### <span data-ttu-id="84a22-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="84a22-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="84a22-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84a22-137">NOTES</span></span>

## <span data-ttu-id="84a22-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84a22-138">RELATED LINKS</span></span>
