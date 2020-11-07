---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910281"
---
# <span data-ttu-id="5a891-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a891-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5a891-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a891-102">SYNOPSIS</span></span>
<span data-ttu-id="5a891-103">Удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="5a891-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="5a891-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a891-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a891-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a891-105">DESCRIPTION</span></span>
<span data-ttu-id="5a891-106">Командлет **Remove-AzKeyVaultCertificateOperation** удаляет операцию с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="5a891-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="5a891-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a891-107">EXAMPLES</span></span>

### <span data-ttu-id="5a891-108">Пример 1: Удаление операции с сертификатом</span><span class="sxs-lookup"><span data-stu-id="5a891-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="5a891-109">Эта команда удаляет операцию с сертификатом с именем TestCert01 из хранилища ключей ContosoKV01 без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5a891-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="5a891-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a891-110">PARAMETERS</span></span>

### <span data-ttu-id="5a891-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a891-111">-DefaultProfile</span></span>
<span data-ttu-id="5a891-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a891-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a891-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5a891-113">-Force</span></span>
<span data-ttu-id="5a891-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a891-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a891-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a891-115">-Name</span></span>
<span data-ttu-id="5a891-116">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="5a891-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="5a891-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a891-117">-PassThru</span></span>
<span data-ttu-id="5a891-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5a891-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a891-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5a891-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a891-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a891-120">-VaultName</span></span>
<span data-ttu-id="5a891-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="5a891-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5a891-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a891-122">-Confirm</span></span>
<span data-ttu-id="5a891-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a891-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a891-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a891-124">-WhatIf</span></span>
<span data-ttu-id="5a891-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a891-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a891-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a891-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a891-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a891-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a891-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a891-128">CommonParameters</span></span>
<span data-ttu-id="5a891-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a891-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a891-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a891-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a891-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a891-131">INPUTS</span></span>

### <span data-ttu-id="5a891-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a891-132">None</span></span>
<span data-ttu-id="5a891-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5a891-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a891-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a891-134">OUTPUTS</span></span>

### <span data-ttu-id="5a891-135">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a891-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5a891-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a891-136">NOTES</span></span>

## <span data-ttu-id="5a891-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a891-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a891-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a891-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="5a891-139">Остановить-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a891-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

