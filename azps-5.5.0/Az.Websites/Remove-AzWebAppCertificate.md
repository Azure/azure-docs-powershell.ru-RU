---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216500"
---
# <span data-ttu-id="8e182-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="8e182-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="8e182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e182-102">SYNOPSIS</span></span>
<span data-ttu-id="8e182-103">Создает сертификат, управляемый службой приложений для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8e182-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="8e182-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e182-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e182-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e182-105">DESCRIPTION</span></span>
<span data-ttu-id="8e182-106">С **помощью cmdlet Remove-AzWebAppCertificate** создается управляемый сертификат Azure App Service Managed Certificate.</span><span class="sxs-lookup"><span data-stu-id="8e182-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="8e182-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e182-107">EXAMPLES</span></span>

### <span data-ttu-id="8e182-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e182-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="8e182-109">Эта команда удаляет сертификат App Service Managed для данного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8e182-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="8e182-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e182-110">PARAMETERS</span></span>

### <span data-ttu-id="8e182-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e182-111">-DefaultProfile</span></span>
<span data-ttu-id="8e182-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e182-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e182-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e182-113">-ResourceGroupName</span></span>
<span data-ttu-id="8e182-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e182-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e182-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="8e182-115">-ThumbPrint</span></span>
<span data-ttu-id="8e182-116">Thumbprint of the certificate that already exists in web space.</span><span class="sxs-lookup"><span data-stu-id="8e182-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e182-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e182-117">CommonParameters</span></span>
<span data-ttu-id="8e182-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e182-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e182-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e182-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e182-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e182-120">INPUTS</span></span>

### <span data-ttu-id="8e182-121">Нет</span><span class="sxs-lookup"><span data-stu-id="8e182-121">None</span></span>

## <span data-ttu-id="8e182-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e182-122">OUTPUTS</span></span>

### <span data-ttu-id="8e182-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e182-123">System.Void</span></span>

## <span data-ttu-id="8e182-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e182-124">NOTES</span></span>

## <span data-ttu-id="8e182-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e182-125">RELATED LINKS</span></span>
[<span data-ttu-id="8e182-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="8e182-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
