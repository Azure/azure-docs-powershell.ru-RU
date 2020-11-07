---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913338"
---
# <span data-ttu-id="415f0-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="415f0-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="415f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="415f0-102">SYNOPSIS</span></span>
<span data-ttu-id="415f0-103">Удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="415f0-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="415f0-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415f0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="415f0-105">DESCRIPTION</span></span>
<span data-ttu-id="415f0-106">Командлет **Remove-AzureKeyVaultCertificateOperation** удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="415f0-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="415f0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="415f0-107">EXAMPLES</span></span>

### <span data-ttu-id="415f0-108">Пример 1: Удаление операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="415f0-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="415f0-109">Эта команда удаляет операцию с сертификатом с именем TestCert01 из хранилища ключей ContosoKV01 без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="415f0-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="415f0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="415f0-110">PARAMETERS</span></span>

### <span data-ttu-id="415f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415f0-111">-DefaultProfile</span></span>
<span data-ttu-id="415f0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="415f0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="415f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="415f0-113">-Force</span></span>
<span data-ttu-id="415f0-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="415f0-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="415f0-115">-Name</span></span>
<span data-ttu-id="415f0-116">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="415f0-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="415f0-117">-PassThru</span></span>
<span data-ttu-id="415f0-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="415f0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="415f0-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="415f0-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="415f0-120">-VaultName</span></span>
<span data-ttu-id="415f0-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="415f0-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="415f0-122">-Confirm</span></span>
<span data-ttu-id="415f0-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="415f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415f0-124">-WhatIf</span></span>
<span data-ttu-id="415f0-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="415f0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415f0-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="415f0-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415f0-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="415f0-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415f0-128">CommonParameters</span></span>
<span data-ttu-id="415f0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="415f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415f0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415f0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415f0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="415f0-131">INPUTS</span></span>

## <span data-ttu-id="415f0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="415f0-132">OUTPUTS</span></span>

### <span data-ttu-id="415f0-133">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="415f0-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="415f0-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="415f0-134">NOTES</span></span>

## <span data-ttu-id="415f0-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="415f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="415f0-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="415f0-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="415f0-137">Остановить-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="415f0-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

