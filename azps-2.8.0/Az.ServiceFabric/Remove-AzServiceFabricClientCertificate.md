---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: d2488792b5893e3972aa27ce98f87a23cec23073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903749"
---
# <span data-ttu-id="9733e-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9733e-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="9733e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9733e-102">SYNOPSIS</span></span>
<span data-ttu-id="9733e-103">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="9733e-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="9733e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9733e-104">SYNTAX</span></span>

### <span data-ttu-id="9733e-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="9733e-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9733e-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="9733e-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9733e-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="9733e-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9733e-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="9733e-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9733e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9733e-109">DESCRIPTION</span></span>
<span data-ttu-id="9733e-110">С помощью средства **Remove-AzServiceFabricClientCertificate** можно удалить из домена клиентские сертификаты или имена субъектов сертификатов для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="9733e-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="9733e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9733e-111">EXAMPLES</span></span>

### <span data-ttu-id="9733e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9733e-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="9733e-113">Эта команда удалит сертификат клиента с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" из кластера.</span><span class="sxs-lookup"><span data-stu-id="9733e-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="9733e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9733e-114">PARAMETERS</span></span>

### <span data-ttu-id="9733e-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="9733e-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="9733e-116">Укажите отпечаток сертификата клиента с разрешением администратора.</span><span class="sxs-lookup"><span data-stu-id="9733e-116">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="9733e-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="9733e-118">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9733e-118">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="9733e-119">-CommonName</span></span>
<span data-ttu-id="9733e-120">Указание общего имени сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="9733e-120">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9733e-121">-DefaultProfile</span></span>
<span data-ttu-id="9733e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9733e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9733e-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="9733e-123">-IssuerThumbprint</span></span>
<span data-ttu-id="9733e-124">Указание отпечатка поставщика сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="9733e-124">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9733e-125">-Name</span></span>
<span data-ttu-id="9733e-126">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9733e-126">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="9733e-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="9733e-128">Укажите отпечаток сертификата клиента с разрешением только на чтение</span><span class="sxs-lookup"><span data-stu-id="9733e-128">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9733e-129">-ResourceGroupName</span></span>
<span data-ttu-id="9733e-130">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9733e-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9733e-131">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="9733e-131">-Thumbprint</span></span>
<span data-ttu-id="9733e-132">Указание отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="9733e-132">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9733e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9733e-133">-Confirm</span></span>
<span data-ttu-id="9733e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9733e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9733e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9733e-135">-WhatIf</span></span>
<span data-ttu-id="9733e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9733e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9733e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9733e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9733e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9733e-138">CommonParameters</span></span>
<span data-ttu-id="9733e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9733e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9733e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9733e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9733e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9733e-141">INPUTS</span></span>

### <span data-ttu-id="9733e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9733e-142">System.String</span></span>

### <span data-ttu-id="9733e-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="9733e-143">System.String[]</span></span>

### <span data-ttu-id="9733e-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="9733e-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="9733e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9733e-145">OUTPUTS</span></span>

### <span data-ttu-id="9733e-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9733e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9733e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="9733e-147">NOTES</span></span>

## <span data-ttu-id="9733e-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9733e-148">RELATED LINKS</span></span>

[<span data-ttu-id="9733e-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9733e-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
