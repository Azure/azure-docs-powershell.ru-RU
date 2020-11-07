---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914569"
---
# <span data-ttu-id="cd376-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="cd376-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="cd376-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd376-102">SYNOPSIS</span></span>
<span data-ttu-id="cd376-103">Создание конфигурации сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cd376-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd376-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd376-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd376-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd376-105">DESCRIPTION</span></span>
<span data-ttu-id="cd376-106">Командлет **New-AzureRmVmssVaultCertificateConfig** указывает секрет, который должен быть размещен на виртуальных машинах с установленной масштабируемостью виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cd376-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="cd376-107">Выходные данные этого командлета предназначены для использования с командлетом Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="cd376-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="cd376-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd376-108">EXAMPLES</span></span>

### <span data-ttu-id="cd376-109">Пример 1: создание конфигурации сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="cd376-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="cd376-110">Эта команда создает конфигурацию сертификата хранилища ключей, в которой используется хранилище сертификатов с именем MyCerts, расположенное по указанному URL-адресу сертификата.</span><span class="sxs-lookup"><span data-stu-id="cd376-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="cd376-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd376-111">PARAMETERS</span></span>

### <span data-ttu-id="cd376-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="cd376-112">-CertificateStore</span></span>
<span data-ttu-id="cd376-113">Указывает хранилище сертификатов на виртуальных машинах в масштабе, где он добавляется.</span><span class="sxs-lookup"><span data-stu-id="cd376-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="cd376-114">Это допустимо только для наборов масштабирования виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="cd376-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd376-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="cd376-115">-CertificateUrl</span></span>
<span data-ttu-id="cd376-116">Задает универсальный код ресурса (URI) сертификата, хранящегося в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cd376-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="cd376-117">Это кодировка Base64 для следующего объекта JSON, который кодируется в кодировке UTF-8:</span><span class="sxs-lookup"><span data-stu-id="cd376-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="cd376-118">{"Data": " \<Base64-encoded-certificate\> ", "тип данных": "PFX", "пароль": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="cd376-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd376-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd376-119">-DefaultProfile</span></span>
<span data-ttu-id="cd376-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd376-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd376-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd376-121">-Confirm</span></span>
<span data-ttu-id="cd376-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd376-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd376-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd376-123">-WhatIf</span></span>
<span data-ttu-id="cd376-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd376-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd376-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd376-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd376-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd376-126">CommonParameters</span></span>
<span data-ttu-id="cd376-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd376-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd376-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd376-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd376-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd376-129">INPUTS</span></span>

### <span data-ttu-id="cd376-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="cd376-130">None</span></span>
<span data-ttu-id="cd376-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cd376-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd376-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd376-132">OUTPUTS</span></span>

###  
<span data-ttu-id="cd376-133">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cd376-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cd376-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd376-134">NOTES</span></span>

## <span data-ttu-id="cd376-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd376-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd376-136">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="cd376-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
