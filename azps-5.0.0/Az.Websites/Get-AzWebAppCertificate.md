---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245994"
---
# <span data-ttu-id="1d1f6-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="1d1f6-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="1d1f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1f6-103">Получает сертификат веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="1d1f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d1f6-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d1f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="1d1f6-106">Командлет **Get-AzWebAppCertificate** получает сведения о сертификатах веб-приложения Azure, связанных с определенной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="1d1f6-107">Если вы знаете отпечаток сертификата, вы также можете использовать этот командлет для получения сведений об указанном сертификате.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="1d1f6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d1f6-108">EXAMPLES</span></span>

### <span data-ttu-id="1d1f6-109">Пример 1: получение сертификатов веб-приложения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d1f6-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1d1f6-110">Эта команда возвращает сведения о загруженных сертификатах веб-приложения, связанных с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="1d1f6-111">Пример 2: получение указанного сертификата веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1d1f6-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1d1f6-112">Эта команда получает сертификат веб-приложения ContosoResourceGroup с отпечатком E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="1d1f6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d1f6-113">PARAMETERS</span></span>

### <span data-ttu-id="1d1f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1f6-114">-DefaultProfile</span></span>
<span data-ttu-id="1d1f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d1f6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d1f6-116">-ResourceGroupName</span></span>
<span data-ttu-id="1d1f6-117">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="1d1f6-118">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="1d1f6-118">-Thumbprint</span></span>
<span data-ttu-id="1d1f6-119">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="1d1f6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1f6-120">CommonParameters</span></span>
<span data-ttu-id="1d1f6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d1f6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1f6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d1f6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1f6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d1f6-123">INPUTS</span></span>

### <span data-ttu-id="1d1f6-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="1d1f6-124">None</span></span>

## <span data-ttu-id="1d1f6-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d1f6-125">OUTPUTS</span></span>

### <span data-ttu-id="1d1f6-126">Microsoft. Azure. Commands. Apps. WebApp. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="1d1f6-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="1d1f6-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d1f6-127">NOTES</span></span>

## <span data-ttu-id="1d1f6-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d1f6-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d1f6-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1d1f6-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

