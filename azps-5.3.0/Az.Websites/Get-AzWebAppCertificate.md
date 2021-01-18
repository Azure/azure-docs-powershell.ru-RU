---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505793"
---
# <span data-ttu-id="32a57-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="32a57-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="32a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a57-102">SYNOPSIS</span></span>
<span data-ttu-id="32a57-103">Получает сертификат Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="32a57-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="32a57-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32a57-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a57-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32a57-105">DESCRIPTION</span></span>
<span data-ttu-id="32a57-106">С **помощью cmdlet get-AzWebAppCertificate** можно получить сведения о сертификатах Azure Web App, связанных с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32a57-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="32a57-107">Если вы знаете свой эскиз сертификата, с помощью этого cmdlet можно получить сведения о указанном сертификате.</span><span class="sxs-lookup"><span data-stu-id="32a57-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="32a57-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32a57-108">EXAMPLES</span></span>

### <span data-ttu-id="32a57-109">Пример 1. Получить сертификаты Web App в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="32a57-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="32a57-110">Эта команда возвращает сведения о загруженных сертификатах Web App, связанных с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="32a57-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="32a57-111">Пример 2. Получить указанный сертификат веб-приложения</span><span class="sxs-lookup"><span data-stu-id="32a57-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="32a57-112">Эта команда получает сертификат ContosoResourceGroup Web App с эскизом E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="32a57-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="32a57-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32a57-113">PARAMETERS</span></span>

### <span data-ttu-id="32a57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a57-114">-DefaultProfile</span></span>
<span data-ttu-id="32a57-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32a57-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a57-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a57-116">-ResourceGroupName</span></span>
<span data-ttu-id="32a57-117">Имя группы ресурсов, которая назначена сертификату.</span><span class="sxs-lookup"><span data-stu-id="32a57-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a57-118">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="32a57-118">-Thumbprint</span></span>
<span data-ttu-id="32a57-119">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="32a57-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a57-120">CommonParameters</span></span>
<span data-ttu-id="32a57-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a57-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a57-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a57-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32a57-123">INPUTS</span></span>

### <span data-ttu-id="32a57-124">Нет</span><span class="sxs-lookup"><span data-stu-id="32a57-124">None</span></span>

## <span data-ttu-id="32a57-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32a57-125">OUTPUTS</span></span>

### <span data-ttu-id="32a57-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="32a57-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="32a57-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32a57-127">NOTES</span></span>

## <span data-ttu-id="32a57-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32a57-128">RELATED LINKS</span></span>

[<span data-ttu-id="32a57-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="32a57-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


