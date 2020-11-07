---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
ms.openlocfilehash: dcdba23de872ed0f1518188387c6f7e2d357c909
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913533"
---
# <span data-ttu-id="f137a-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f137a-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="f137a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f137a-102">SYNOPSIS</span></span>
<span data-ttu-id="f137a-103">Получает сертификат веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f137a-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f137a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f137a-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f137a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f137a-105">DESCRIPTION</span></span>
<span data-ttu-id="f137a-106">Командлет **Get-AzureRmWebAppCertificate** получает сведения о сертификатах веб-приложения Azure, связанных с определенной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f137a-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="f137a-107">Если вы знаете отпечаток сертификата, вы также можете использовать этот командлет для получения сведений об указанном сертификате.</span><span class="sxs-lookup"><span data-stu-id="f137a-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="f137a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f137a-108">EXAMPLES</span></span>

### <span data-ttu-id="f137a-109">Пример 1: получение сертификатов веб-приложения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f137a-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f137a-110">Эта команда возвращает сведения о загруженных сертификатах веб-приложения, связанных с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f137a-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f137a-111">Пример 2: получение указанного сертификата веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f137a-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f137a-112">Эта команда получает сертификат веб-приложения ContosoResourceGroup с отпечатком E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="f137a-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="f137a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f137a-113">PARAMETERS</span></span>

### <span data-ttu-id="f137a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f137a-114">-DefaultProfile</span></span>
<span data-ttu-id="f137a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f137a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f137a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f137a-116">-ResourceGroupName</span></span>
<span data-ttu-id="f137a-117">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="f137a-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f137a-118">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="f137a-118">-Thumbprint</span></span>
<span data-ttu-id="f137a-119">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="f137a-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f137a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f137a-120">CommonParameters</span></span>
<span data-ttu-id="f137a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f137a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f137a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f137a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f137a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f137a-123">INPUTS</span></span>

### <span data-ttu-id="f137a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="f137a-124">None</span></span>
<span data-ttu-id="f137a-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f137a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f137a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f137a-126">OUTPUTS</span></span>

## <span data-ttu-id="f137a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f137a-127">NOTES</span></span>

## <span data-ttu-id="f137a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f137a-128">RELATED LINKS</span></span>

[<span data-ttu-id="f137a-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f137a-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


