---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557643"
---
# <span data-ttu-id="3ba06-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ba06-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="3ba06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ba06-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba06-103">Создает экземпляр PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3ba06-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ba06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ba06-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ba06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba06-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba06-106">Командлет **New-AzureRmApiManagementHostnameConfiguration** является вспомогательной командой, которая создает экземпляр **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3ba06-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="3ba06-107">Эта команда используется с командлетом Set-AzureRmApiManagementHostnames.</span><span class="sxs-lookup"><span data-stu-id="3ba06-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="3ba06-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ba06-108">EXAMPLES</span></span>

### <span data-ttu-id="3ba06-109">Пример 1: создание и инициализация экземпляра PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ba06-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="3ba06-110">Эта команда создает и инициализирует экземпляр **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3ba06-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="3ba06-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ba06-111">PARAMETERS</span></span>

### <span data-ttu-id="3ba06-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3ba06-112">-CertificateThumbprint</span></span>
<span data-ttu-id="3ba06-113">Указывает отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="3ba06-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="3ba06-114">Сертификат необходимо сначала импортировать с помощью командлета Import-AzureRmApiManagementHostnameCertificate.</span><span class="sxs-lookup"><span data-stu-id="3ba06-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba06-115">-DefaultProfile</span></span>
<span data-ttu-id="3ba06-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3ba06-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3ba06-117">-Hostname</span></span>
<span data-ttu-id="3ba06-118">Задает настраиваемое имя узла, для которого этот командлет создает экземпляр **PsApiManagementHostnameConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="3ba06-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba06-119">CommonParameters</span></span>
<span data-ttu-id="3ba06-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ba06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba06-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba06-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba06-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ba06-122">INPUTS</span></span>

### <span data-ttu-id="3ba06-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ba06-123">None</span></span>
<span data-ttu-id="3ba06-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ba06-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ba06-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba06-125">OUTPUTS</span></span>

### <span data-ttu-id="3ba06-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ba06-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="3ba06-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ba06-127">NOTES</span></span>

## <span data-ttu-id="3ba06-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ba06-128">RELATED LINKS</span></span>

[<span data-ttu-id="3ba06-129">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba06-129">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="3ba06-130">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3ba06-130">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


